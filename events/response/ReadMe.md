> Manny Ferrario
> 04/18/2019

# Telemetry Response Event

Services record their responses to incoming requests as Response telemetry events.

If the service encounters an error, it should generate an Error event. Otherwise, there will not be context for troubleshooting later. Moreover, error metrics should be tracked using the Error telemetry event - not the response event.

For a detailed description of the Response Event object, please refer to [Telemetry Data Specification](https://confluence.rccl.com/display/EEE/Telemetry+Data+Specification).

## Response Event

The following snippet is an example of a response event thrown by web application.

```json
{
  "datetime": "2018-10-16T10:14:38.335122-04:00",

  "evtType": "Response",
  "feature": "GA",
  "source": "Excalibur-Web-App",
  "vers": "1.3.13",

  "status": 200,
  "success": true,
  "latency": 380,
  "dest": "ProfileBookings",
  "operation": "GetProfile",
  "context": "vdsId=G7010131",

  "eventId": "56c790bc-a2e1-4eb7-92c2-8129b59bc1c9",
  "traceId": "e4db12f2-b176-432a-a7a6-8bb3ed08beeb",

  "env": "AWS",
  "device": "desktop",
  "platform": "ios",

  "userId": "G7010131",
  "sessionId": "9a0fa33b-e292-46b1-8d34-660d0c35d64f"
}
```

## Validation Schema

The following schema can be used to validate your schema.

> [Error Schema](./response-schema.json)

## Validation Tool

An online, interactive JSON Schema validator. Supports JSON Schema Draft 3, Draft 4, Draft 6 and Draft 7.

> https://www.jsonschemavalidator.net
