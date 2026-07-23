# Santander UK (santander-uk)

Santander UK plc is a major British retail and commercial bank and one of the CMA9 banks mandated to deliver UK Open Banking. It is a wholly owned, ring-fenced subsidiary of Banco Santander S.A. of Madrid, Spain, formed from the former Abbey National, Alliance & Leicester, and the savings business of Bradford & Bingley. Authorised by the Prudential Regulation Authority and regulated by the FCA and PRA, it serves around 14 million active personal, business, and corporate customers and publishes a public developer portal ("Santander Developers") under PSD2 and the CMA Order.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/santander-uk/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/santander-uk/refs/heads/main/apis.yml)

## Tags

- Financial Services
- Banking
- Open Banking
- PSD2
- OBIE
- CMA9
- United Kingdom
- Payments
- Account Information
- FAPI

## Timestamps

- **Created:** 2026-07-23
- **Modified:** 2026-07-23

## APIs

### Santander UK Open Data API

Free, public, unauthenticated Open Data reference API publishing Santander UK ATMs, branches, and product information (personal & business current accounts, unsecured SME loans, commercial credit cards) per the OBIE Open Data standard.

- **Human URL:** [https://api-portal.omni.slz.santander.co.uk/external/opendata/atms](https://api-portal.omni.slz.santander.co.uk/external/opendata/atms)
- **Base URL:** `https://api-portal.omni.slz.santander.co.uk/external/opendata`

#### Tags

- Open Data
- ATMs
- Branches
- Products

#### Properties

- [OpenAPI](openapi/obie-opendata-swagger.json) — OBIE Open Data API standard (Swagger 2.0)
- [Documentation](https://api-portal.omni.slz.santander.co.uk/external/opendata/atms)

### Santander UK Account & Transaction Information API

OBIE Read/Write Account and Transaction Information (AIS) API for accessing account, balance, transaction, and party data with customer consent. FAPI-secured (OAuth2/OIDC, mTLS, PSD2 SCA).

- **Human URL:** [https://developer.santander.co.uk/sanuk/external/product](https://developer.santander.co.uk/sanuk/external/product)
- **Base URL:** `https://openbanking.santander.co.uk/open-banking/v3.1/aisp`

#### Tags

- Account Information
- AIS
- Read/Write

#### Properties

- [OpenAPI](openapi/obie-account-info-openapi.yaml) — OBIE Account & Transaction API standard (OpenAPI 3.0)
- [Documentation](https://developer.santander.co.uk/sanuk/external/product)

### Santander UK Payment Initiation API

OBIE Read/Write Payment Initiation (PIS) API for initiating domestic, scheduled, standing-order, international, and file payments on behalf of customers. FAPI-secured (OAuth2/OIDC, mTLS, PSD2 SCA).

- **Human URL:** [https://developer.santander.co.uk/sanuk/external/product](https://developer.santander.co.uk/sanuk/external/product)
- **Base URL:** `https://openbanking.santander.co.uk/open-banking/v3.1/pisp`

#### Tags

- Payment Initiation
- PIS
- Read/Write

#### Properties

- [OpenAPI](openapi/obie-payment-initiation-openapi.yaml) — OBIE Payment Initiation API standard (OpenAPI 3.0)
- [Documentation](https://developer.santander.co.uk/sanuk/external/product)

### Santander UK Confirmation of Funds API

OBIE Read/Write Confirmation of Funds (CBPII) API allowing an authorised card-based payment instrument issuer to confirm the availability of funds on a customer account. FAPI-secured (OAuth2/OIDC, mTLS, PSD2 SCA).

- **Human URL:** [https://developer.santander.co.uk/sanuk/external/product](https://developer.santander.co.uk/sanuk/external/product)
- **Base URL:** `https://openbanking.santander.co.uk/open-banking/v3.1/cbpii`

#### Tags

- Confirmation of Funds
- CBPII
- Read/Write

#### Properties

- [OpenAPI](openapi/obie-confirmation-funds-openapi.yaml) — OBIE Confirmation of Funds API standard (OpenAPI 3.0)
- [Documentation](https://developer.santander.co.uk/sanuk/external/product)

## Common Properties

- [Website](https://www.santander.co.uk/)
- [Developer Portal](https://developer.santander.co.uk/sanuk/external/)
- [Documentation](https://developer.santander.co.uk/sanuk/external/product)
- [Sandbox](https://sandbox-developer.santander.co.uk/sanuk/external-sandbox/faq-page)
- [LinkedIn](https://www.linkedin.com/company/santander-uk)
- [Status Page](https://www.santander.co.uk/personal/support/service-status)
- [About](https://www.santander.co.uk/about-santander)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
