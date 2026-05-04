# API Requirements

## Purpose

Define example API considerations for mobile session timeout and authentication behavior.

## Example API Needs

### Get Client Timeout Configuration

Endpoint:

```http
GET /clients/{clientId}/security-settings
{
  "clientId": "12345",
  "mobileTimeoutMinutes": 15,
  "warningBeforeTimeoutMinutes": 2,
  "ssoEnabled": true
}
