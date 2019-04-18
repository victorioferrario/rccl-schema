> Manny Ferrario
> 04/18/2019

# Telemetry Request Event

Request Events are used to track simple metrics information when micro-services or applications make outgoing requests. A request event can be used for outgoing HTTP REST API calls or calls to any server API/SDK (e.g. calling a database or cache). Some example use cases that would generate a request event includes:

A mobile or web app calls an Excalibur micro-service. The app generates a request event for the call.
A micro-service calls another micro-service to fulfill a service request it received from an app. The calling micro-service generates a request event for the call.
A micro-service queries a database or cache. The micro-service records this as a request event.
A micro-service queries a 3rd party system like Savyint. The micro-service records this as a request event.
For a detailed description of the Request Event object, please refer to [Telemetry Data Specification](https://confluence.rccl.com/display/EEE/Telemetry+Data+Specification).

## Request Event

The following snippet is an example of a request event thrown by web application.

```json
{
  "datetime": "2018-10-16T10:14:38.335122-04:00",

  "evtType": "Request",
  "feature": "GA",
  "source": "Excalibur-Web-App",
  "vers": "1.3.13",

  "dest": "ProfileBookings",
  "operation": "GetProfile",
  "method": "POST",
  "context": "vdsId=G7010131",
  "path": "/api/v1/profile/1234",
  "retries": 0,
  "latency": 380,
  "status": 200,
  "success": true,

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

> [Error Schema](./request-schema.json)

## Validation Tool

An online, interactive JSON Schema validator. Supports JSON Schema Draft 3, Draft 4, Draft 6 and Draft 7.

> https://www.jsonschemavalidator.net
