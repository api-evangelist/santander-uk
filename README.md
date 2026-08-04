# Santander UK (santander-uk)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
