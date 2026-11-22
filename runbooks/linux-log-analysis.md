
# Linux Log Analysis for Application Support

## Purpose
This runbook explains how to review Linux logs during application troubleshooting.

## Common Commands

### 1. View the last 50 log lines
```bash
tail -n 50 /var/log/syslog
```

### 2. Monitor logs in real time
```bash
tail -f /var/log/syslog
```

### 3. Search for errors
```bash
grep -i "error" /var/log/syslog
```

### 4. Search for failed operations
```bash
grep -i "failed" /var/log/syslog
```

### 5. Search for a specific request ID
```bash
grep "lab-corr-001" booking-api.log
```

## Troubleshooting Scenario

A user reports that the booking application is failing.

## Investigation Steps
1. Confirm the issue start time.
2. Identify the affected application or service.
3. Review logs around the reported timestamp.
4. Search for error messages or exceptions.
5. Check the correlation ID if available.
6. Compare failed requests with successful requests.
7. Document findings in the incident ticket.

## Important Notes
- Log file locations may differ between Linux distributions.
- Use approved access permissions.
- Do not share passwords, tokens, or sensitive customer information.
- Escalate if the issue requires administrator access.
