---
name: Access Santander UK account and transaction data (AIS)
description: Obtain customer consent then read accounts, balances, and transactions via the OBIE Account & Transaction (AIS) API.
api: openapi/obie-account-info-openapi.yaml
operations: [CreateAccountAccessConsents, GetAccounts, GetAccountsAccountIdBalances, GetAccountsAccountIdTransactions]
---

# Access Santander UK account and transaction data (AIS)

Use the OBIE Read/Write Account & Transaction Information API to read a customer's
account data as an authorised AISP. All calls require FAPI-grade OAuth2/OIDC over
mutual-TLS with an eIDAS/OBIE certificate; see `authentication/santander-uk-authentication.yml`
and `conventions/santander-uk-conventions.yml`.

## Steps

1. **Authenticate as the TPP.** Obtain a client-credentials access token with the
   `accounts` scope (`TPPOAuth2Security`).
2. **Create an account-access consent.** Call `CreateAccountAccessConsents` with the
   requested `Permissions` (e.g. `ReadAccountsDetail`, `ReadBalances`,
   `ReadTransactionsDetail`). Send a unique `x-idempotency-key` and `x-fapi-interaction-id`.
3. **Redirect the PSU for authorisation (SCA).** Use the authorization-code flow
   (`PSUOAuth2Security`) so the customer completes PSD2 strong customer authentication
   and authorises the consent.
4. **List authorised accounts.** Call `GetAccounts` with the PSU access token.
5. **Read balances.** Call `GetAccountsAccountIdBalances` for each `AccountId`.
6. **Read transactions.** Call `GetAccountsAccountIdTransactions`; page through results
   using the `Links.Next` field (see pagination in the conventions file).

## Rules

- Echo `x-fapi-interaction-id` from every response for tracing.
- Handle the OBIE `OBErrorResponse1` envelope on 4xx/5xx (see `errors/santander-uk-problem-types.yml`).
- A 403 means the consent lacks the required permission/scope; a 401 means the token
  or SCA is invalid/expired.
