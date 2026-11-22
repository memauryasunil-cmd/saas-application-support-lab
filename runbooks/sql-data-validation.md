
# SQL Data Validation for Application Support

## Purpose
Use SQL queries to validate application data during troubleshooting.

**Safety:** These are sample queries for a test database. Use read-only access and follow company authorization procedures.

## Scenario
A user reports that booking ID 1042 is not showing the expected booking status.

## Step 1: Check Booking Record

```sql
SELECT booking_id, booking_status, created_at
FROM bookings
WHERE booking_id = 1042;
```

## Step 2: Check Booking Status Counts

```sql
SELECT booking_status, COUNT(*) AS total
FROM bookings
GROUP BY booking_status;
```

## Step 3: Check Recent Bookings

```sql
SELECT booking_id, booking_status, created_at
FROM bookings
WHERE created_at >= CURRENT_DATE - INTERVAL '1 day'
ORDER BY created_at DESC;
```

## Troubleshooting Approach
1. Confirm the booking ID with the user.
2. Check whether the record exists.
3. Verify the current booking status.
4. Compare with expected application behavior.
5. Share findings with the application or database team if needed.

## Important SQL Safety Practices
- Use SELECT queries for investigation.
- Filter results using WHERE.
- Select only required columns.
- Never expose customer personal information.
- Do not run UPDATE or DELETE without approval.
- Never modify production data without authorization.
