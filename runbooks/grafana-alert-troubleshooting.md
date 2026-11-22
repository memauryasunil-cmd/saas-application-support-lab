
# Grafana Alert Troubleshooting Runbook

## Purpose
This runbook provides a structured approach to investigating monitoring alerts in a simulated SaaS environment.

## Alert Investigation Steps

### 1. Acknowledge the Alert
- Check the alert name and severity.
- Note the alert start time.
- Identify the affected service or server.

### 2. Review the Grafana Dashboard
- Check CPU, memory, disk, and network metrics.
- Compare current values with historical trends.
- Identify whether the issue is continuous or temporary.

### 3. Check Alert Details
- Review the configured threshold.
- Check the alert evaluation period.
- Identify the metric or query that triggered the alert.

### 4. Investigate the Server
Use Linux commands where appropriate:

```bash
top
```

Check CPU and memory usage.

```bash
ps aux --sort=-%cpu | head
```

Identify processes consuming high CPU.

```bash
free -h
```

Check memory utilization.

```bash
df -h
```

Check disk space.

### 5. Review Application Logs
- Check logs around the alert timestamp.
- Look for errors or unusual activity.
- Correlate application logs with monitoring metrics.

### 6. Resolve or Escalate
- Follow approved operational procedures.
- Avoid terminating critical processes without authorization.
- Escalate to the infrastructure or application team if required.

### 7. Validate Recovery
- Confirm metrics return to normal.
- Check whether the alert clears.
- Verify application availability and response time.

## Incident Documentation
Record:
- Alert name
- Timestamp
- Affected service
- Metrics observed
- Troubleshooting performed
- Root cause
- Resolution
- Preventive actions

## Important Note
This runbook is for a simulated portfolio lab. Commands should be used only in an authorized test environment.
