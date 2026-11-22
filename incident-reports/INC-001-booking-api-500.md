
# Incident INC-001: Booking API returns HTTP 500

## Incident Summary
- Status: Resolved (Simulated)
- Service: booking-api
- Severity: High
- Issue: Booking API is returning HTTP 500 error.

## User Report
"Booking confirmation fails after submitting the booking."

## Troubleshooting Steps
1. Confirmed the issue affects multiple test requests.
2. Checked the API response status code.
3. Collected timestamp and correlation ID.
4. Reviewed application logs.
5. Identified a missing configuration value.

## Root Cause
The simulated booking service was missing the required configuration value `PAYMENT_PROVIDER_MODE`.

Because of this, the application returned HTTP 500.

## Resolution
1. Corrected the configuration in the simulated lab.
2. Restarted the service using the approved procedure.
3. Tested the booking API again.
4. Confirmed the booking request succeeded.

## Preventive Actions
- Validate required configuration at startup.
- Improve error logging.
- Add a health check.
- Add a regression test.

## Learning
HTTP 500 indicates a server-side error. To find the root cause, we need to check logs, timestamps, correlation IDs, and recent changes.
