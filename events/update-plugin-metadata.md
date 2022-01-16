# Update Plugin Metadata

## Summary

Sent by the server to client after initial connection.

## Specification

### UpdateMetadataEvent

| Fieldname  | Type   | Description                  |
| ---------- | ------ | ---------------------------- |
| pluginId   | string | Your unique plugin id        |
| pluginName | string | Your plugin name for display |

## Example

```json
{
    "pluginId": "portfolio",
    "pluginName": "Portfolio
}
```
