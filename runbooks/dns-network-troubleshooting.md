
# DNS and Network Troubleshooting

## Purpose
This runbook describes a basic troubleshooting process for DNS, network connectivity, and VPN-related issues.

## Scenario
A user reports that the SaaS application is not opening on their system.

## Step 1: Check Network Connectivity

```bash
ping 8.8.8.8
```

This checks basic IP connectivity. Ping may be blocked by some networks.

## Step 2: Check DNS Resolution

Windows:
```cmd
nslookup example.com
```

Linux:
```bash
dig example.com
```

DNS converts a domain name into an IP address.

## Step 3: Check VPN
- Confirm the VPN client is connected.
- Check whether the user has the correct VPN profile.
- Disconnect and reconnect only according to company policy.
- Verify whether the application requires VPN access.

## Step 4: Check Network Route

Windows:
```cmd
tracert example.com
```

Linux:
```bash
traceroute example.com
```

## Troubleshooting Steps
1. Confirm whether one user or multiple users are affected.
2. Check Wi-Fi or LAN connection.
3. Verify VPN status.
4. Check DNS resolution.
5. Test application access.
6. Record error messages and results.
7. Escalate to the network team if required.

## Important Notes
- Ping failure does not always mean the server is down.
- Do not change firewall or network settings without authorization.
- Record troubleshooting results in the incident ticket.
