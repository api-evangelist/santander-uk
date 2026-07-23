---
name: Initiate a Santander UK domestic payment (PIS)
description: Register a domestic payment consent, obtain PSU authorisation, then initiate the payment via the OBIE Payment Initiation (PIS) API.
api: openapi/obie-payment-initiation-openapi.yaml
operations: [CreateDomesticPaymentConsents, GetDomesticPaymentConsentsConsentIdFundsConfirmation, CreateDomesticPayments, GetDomesticPaymentsDomesticPaymentId]
---

# Initiate a Santander UK domestic payment (PIS)

Use the OBIE Read/Write Payment Initiation API to initiate a domestic payment as an
authorised PISP. Requires FAPI OAuth2/OIDC over mTLS and a detached JWS signature
(`x-jws-signature`) on write operations.

## Steps

1. **Authenticate as the TPP.** Obtain a client-credentials token with the `payments` scope.
2. **Create the payment consent.** Call `CreateDomesticPaymentConsents` with the
   `Initiation` block (amount, creditor account, reference). Include a unique
   `x-idempotency-key` (24h retention) and the `x-jws-signature` header.
3. **Redirect the PSU for authorisation (SCA).** Use the authorization-code flow so the
   customer authorises the specific payment (PSD2 SCA).
4. **(Optional) Confirm funds.** Call `GetDomesticPaymentConsentsConsentIdFundsConfirmation`
   to check funds availability before submitting.
5. **Initiate the payment.** Call `CreateDomesticPayments` referencing the authorised
   `ConsentId`; reuse a fresh `x-idempotency-key` and re-sign with `x-jws-signature`.
6. **Poll payment status.** Call `GetDomesticPaymentsDomesticPaymentId` to track the
   `Status` (e.g. `AcceptedSettlementInProcess`, `AcceptedSettlementCompleted`).

## Rules

- The `Initiation` block in the payment MUST match the consent exactly, or the request is rejected.
- Reuse the same `x-idempotency-key` only for identical retries (idempotent within 24h).
- Handle 409 (idempotency/state conflict) and 422 (unprocessable instruction) per
  `errors/santander-uk-problem-types.yml`.
