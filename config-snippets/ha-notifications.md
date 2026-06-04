# Home Assistant Notification Payloads

Node-RED JSON examples for sending notifications via Home Assistant.

## Using `{{payload}}` (dynamic message)

**Front Door**
```json
{
    "title": "Front Door",
    "message": "{{payload}}",
    "data": {
        "color": "green",
        "channel": "Front_Door",
        "priority": "high",
        "ttl": 0
    }
}
```

**Water Detection**
```json
{
    "title": "WATER IN BASEMENT!",
    "message": "{{payload}}",
    "data": {
        "color": "red",
        "channel": "Network Alert",
        "priority": "high",
        "ttl": 0
    }
}
```

**Dehumidifier**
```json
{
    "title": "Empty Storage Dehumidifier!",
    "message": "Humidity is {{payload}}% - Time to empty!",
    "data": {
        "color": "red",
        "channel": "Dehumidifier",
        "priority": "high",
        "ttl": 0
    }
}
```

**ABS / Service Data Title**
```json
{
    "message": "{{payload.event.service_data.title}}",
    "data": {
        "color": "green",
        "channel": "ABS",
        "priority": "high",
        "ttl": 0
    }
}
```

## Using a custom static message

**Power Grid Alert**
```json
{
    "title": "ON GRID",
    "message": "UNLIMITED POWER",
    "data": {
        "color": "green",
        "channel": "Grid Alert",
        "priority": "high",
        "ttl": 0
    }
}
```
