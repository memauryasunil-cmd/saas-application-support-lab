
# REST API Troubleshooting Checklist

## 1. Understand the Issue
- Confirm the API endpoint.
- Confirm the HTTP method (GET, POST, PUT, DELETE).
- Ask when the issue started.
- Check whether one user or multiple users are affected.

## 2. Check the API Response
- HTTP status code
- Response body
- Request timestamp
- Correlation ID

## 3. Understand HTTP Status Codes
| Status Code | Meaning |
|---|---|
| 200 | Request successful |
| 400 | Bad request |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Resource not found |
| 429 | Too many requests |
| 500 | Internal server error |
| 503 | Service unavailable |

## 4. Troubleshooting
1. Reproduce the issue in a test environment.
2. Verify request parameters and headers.
3. Check authentication and permissions.
4. Review application logs.
5. Check recent deployments or configuration changes.
6. Validate dependent services.

## 5. Resolution
- Apply the approved fix or workaround.
- Retest the API.
- Confirm the issue is resolved.
- Update the incident ticket.
- Document the root cause.
