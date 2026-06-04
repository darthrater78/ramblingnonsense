# WUD — Node-RED Notification JSON

Paste this into a Node-RED JSON node to forward WUD update events as notifications.

```json
{
    "message": "{{payload.event.service_data.title}}\n{{payload.event.service_data.message}}",
    "data": {
        "color": "green",
        "channel": "WUD",
        "priority": "high",
        "ttl": 0
    }
}
```

## Container Label Template

Add these labels to any container you want WUD to track with semantic versioning.
Update `wud.link.template` to point to the project's actual releases page.

```yaml
labels:
  wud.tag.include: ^v?\d+\.\d+\.\d+$
  wud.link.template: https://github.com/OWNER/REPO/releases/tag/$${major}.$${minor}.$${patch}
```
