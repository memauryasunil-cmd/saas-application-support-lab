
# Incident INC-002: Kafka Consumer Lag

## Incident Summary
- Status: Investigating (Simulated)
- Service: booking-event-consumer
- Priority: Medium (example)
- Issue: Kafka messages are being processed with delay.

## User Report
"Booking events are appearing late in the application."

## What is Kafka Consumer Lag?
Consumer lag is the difference between the latest message offset in a Kafka partition and the consumer's current position.

When lag increases, the consumer may be processing messages slower than they are arriving.

## Possible Causes
1. Consumer application is slow.
2. Consumer service is stopped or unhealthy.
3. Message processing is taking too long.
4. Consumer group is rebalancing.
5. Message production rate is higher than consumption rate.

## Troubleshooting Steps
1. Confirm the affected topic and consumer group.
2. Check whether the consumer application is running.
3. Review consumer group lag.
4. Check application logs for processing errors.
5. Review CPU and memory utilization.
6. Check whether the lag is increasing or decreasing.
7. Escalate to the Kafka or application team if required.

## Example Kafka Command

```bash
kafka-consumer-groups.sh \
  --bootstrap-server localhost:9092 \
  --describe \
  --group booking-event-consumer
```

This command displays consumer group information, including current offset, log end offset, and lag.

## Monitoring
Monitor:
- Consumer lag
- Records consumed per second
- Consumer processing errors
- Consumer health
- CPU and memory utilization

## Resolution (Simulated)
The consumer application was processing messages slowly.

The application team reviewed processing time and improved the consumer processing logic.

After the change, consumer lag gradually decreased.

## Preventive Actions
- Monitor consumer lag.
- Set alerts for sustained high lag.
- Review consumer processing performance.
- Maintain application health monitoring.
- Document recurring consumer errors.

## Learning
Kafka consumer lag helps identify whether a consumer is keeping up with incoming messages. Monitoring lag and consumption rate helps support teams detect delayed event processing.
