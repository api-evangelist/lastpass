# LastPass (lastpass)

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
