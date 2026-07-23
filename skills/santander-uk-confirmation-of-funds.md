---
name: Confirm funds availability on a Santander UK account (CBPII)
description: Create a funds-confirmation consent and confirm whether funds are available via the OBIE Confirmation of Funds (CBPII) API.
api: openapi/obie-confirmation-funds-openapi.yaml
operations: [CreateFundsConfirmationConsents, GetFundsConfirmationConsentsConsentId, CreateFundsConfirmations]
---

# Confirm funds availability on a Santander UK account (CBPII)

Use the OBIE Read/Write Confirmation of Funds API as an authorised CBPII (card-based
payment instrument issuer) to check whether funds are available on a customer account.
Requires FAPI OAuth2/OIDC over mTLS.

## Steps

1. **Authenticate as the TPP.** Obtain a client-credentials token with the
   `fundsconfirmations` scope.
2. **Create the funds-confirmation consent.** Call `CreateFundsConfirmationConsents`
   with the debtor account and expiry. Include `x-idempotency-key` and `x-fapi-interaction-id`.
3. **Redirect the PSU for authorisation (SCA).** The customer authorises the CBPII to
   query funds availability.
4. **(Optional) Verify consent status.** Call `GetFundsConfirmationConsentsConsentId`.
5. **Confirm funds.** Call `CreateFundsConfirmations` with the `ConsentId` and the
   `InstructedAmount`; the response `FundsAvailable` boolean states availability.

## Rules

- A funds confirmation is a point-in-time yes/no check; it does not reserve or move funds.
- Handle the OBIE `OBErrorResponse1` envelope on errors (see `errors/santander-uk-problem-types.yml`).
