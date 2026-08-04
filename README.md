# LastPass (lastpass)

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

LastPass is a password and identity-management platform offering personal and enterprise vaults, single sign-on, multi-factor authentication, and directory provisioning. The LastPass Enterprise API and Provisioning API let admins programmatically manage users, groups, shared folders, policies, and events. SCIM and SAML endpoints integrate with identity providers; an MFA SDK supports adaptive authentication for custom apps.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/lastpass/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=lastpass-api-evangelist&utm_content=repo)

## Type

- **x-type:** company

## Tags

- Security, Password Manager, Vault, Identity, Enterprise, SSO, MFA

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-08

## APIs

| API | Description |
|---|---|
| LastPass Enterprise API | Single POST endpoint at `enterpriseapi.php` taking command-style payloads (batchadd, batchchange, deluser, disableuser, getuserdata, getsfdata, getreport). |
| LastPass Provisioning API | User-lifecycle subset of the Enterprise API used by directory connectors. |
| LastPass SCIM API | SCIM 2.0 Users and Groups endpoint for Okta, Entra ID, OneLogin, Google Cloud Identity. |
| LastPass SAML / SSO Endpoint | SAML 2.0 IdP and SP endpoints powering the LastPass App Library. |
| LastPass MFA SDK | Server-side SDK for embedding push, biometric, and TOTP MFA in custom apps. |
| LastPass Reporting Commands | Reporting subset of the Enterprise API (getreport, getevents, getuserdata, getsfdata). |

## Common Properties

- [Website](https://www.lastpass.com/)
- [Documentation](https://support.lastpass.com/help/use-the-lastpass-enterprise-api)
- [Plans](plans/lastpass-plans-pricing.yml) - API Commons Plans 0.1
- [RateLimits](rate-limits/lastpass-rate-limits.yml) - API Commons Rate Limits 0.1
- [FinOps](finops/lastpass-finops.yml) - FOCUS-aligned FinOps Framework 1.0

## Plans

- **Free** - Personal; single device type at a time; no API access.
- **Premium** - $3/month; multi-device, dark-web monitoring, emergency access.
- **Families** - $4/month for 6 users.
- **Teams** - $4/user/month, capped at 50 users; Enterprise API and SCIM included.
- **Business** - $7/user/month; unlimited users; advanced policies, SSO apps.
- **MFA Add-On** - $3/user/month layered on Teams or Business.
- **Identity Bundle** - $8/user/month; Business + MFA + SSO.

## Rate Limits

- Dynamic per-customer throttle on the Enterprise API; sustained excessive volume can trigger temporary block.
- Authentication endpoints apply adaptive backoff, captcha, and lockout on failed login.
- Use batch commands and the SCIM endpoint instead of per-user calls for sync workloads.

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
