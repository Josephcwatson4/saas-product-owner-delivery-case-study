# SSO Workflow

## Objective

Create a repeatable SSO onboarding workflow that reduces client confusion, rework, and implementation delays.

## Supported Authentication Types

- SAML 2.0
- OIDC

## Required Client Inputs

- Identity Provider metadata URL or file
- Entity ID
- Assertion Consumer Service URL
- Signing certificate
- NameID format
- User attribute mappings
- Test user credentials
- Client IT contact

## Workflow

1. Client completes SSO intake form.
2. Implementation validates required metadata.
3. Engineering or configuration team sets up SSO connection.
4. Internal testing confirms authentication behavior.
5. Client IT completes validation testing.
6. Defects or mismatches are resolved.
7. SSO is approved for go-live.

## Validation Checklist

- Metadata received and complete
- Certificate is valid and not expired
- User attributes are mapped correctly
- Test user can authenticate successfully
- Logout behavior is confirmed
- Error handling is documented
- Client approval is received
