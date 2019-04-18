> Manny Ferrario
> 04/18/2019

# Telemetry Error Event

## Error Event

The following snippet is an example of an error event thrown by web application.

```json
{
  "datetime": "2018-10-16T10:14:38.335122-04:00",

  "evtType": "Error",
  "feature": "GA",
  "source": "ProfileService",
  "vers": "1.3.13",

  "errId": "ForgeRock",
  "errMsg": "Call to ForgeRock to GET user profile failed with 500 status.",
  "stack": "...stack trace here...",
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

> [Error Schema](./error-schema.json)

## Validation Tool

An online, interactive JSON Schema validator. Supports JSON Schema Draft 3, Draft 4, Draft 6 and Draft 7.

> https://www.jsonschemavalidator.net
