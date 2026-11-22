
# INC-003: High CPU Usage Alert

## Incident Overview
- Incident ID: INC-003
- Application: Simulated SaaS Application
- Monitoring Tool: Grafana
- Alert: High CPU Usage
- Severity: Medium
- Status: Resolved
- Environment: Simulated Lab

## Incident Description
A Grafana alert was triggered when CPU utilization on the simulated application server exceeded the defined threshold.

The alert indicated that CPU usage remained above 85% for several minutes.

## Business Impact
- Application response time increased.
- Some users experienced slower page loading.
- No data loss was reported in this simulated scenario.

## Troubleshooting Performed
1. Acknowledged the monitoring alert.
2. Checked the CPU utilization dashboard.
3. Reviewed the alert time and affected server.
4. Checked running processes using Linux commands.
5. Reviewed application logs for unusual activity.
6. Identified a simulated background process consuming excessive CPU.

## Root Cause
A simulated background process was consuming unusually high CPU resources, resulting in increased server utilization.

## Resolution
1. Stopped the simulated high-CPU process.
2. Verified CPU utilization decreased.
3. Checked application response time.
4. Confirmed the alert returned to a normal state.

## Preventive Actions
- Review CPU alert thresholds.
- Monitor CPU usage trends.
- Investigate recurring high-CPU processes.
- Add the troubleshooting steps to the runbook.
- Review resource utilization during maintenance.

## Lessons Learned
Monitoring alerts help identify performance issues before they cause a major service disruption.

## Disclaimer
This is a fictional incident created for portfolio demonstration and learning purposes. It does not represent an actual production incident.
