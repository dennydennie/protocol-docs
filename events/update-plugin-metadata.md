# Update Plugin Metadata

## Summary

This event is sent from the plugin to the front end app on each new websocket connection.

It gives the front end app information about the plugin for display to the user.

Note that all fields are required, if not all fields are populated, further messages from the plugin will be ignored.

## Event Specification

### Event Name

`update-metadata`

### Event Fields

| Fieldname      | Type             | Description                                    |
| -------------- | ---------------- | ---------------------------------------------- |
| pluginId\*     | string           | Your unique plugin id                          |
| pluginName\*   | string           | Your plugin name for display                   |
| githubUrl\*    | string           | The link to your your plugin github repository |
| ownerAddress\* | string           | Your public address for revenue share payments |
| ownerChain\*   | 'bsc'\|'polygon' | Your chain for revenue share payments          |

## Examples

### JSON

```json
{
  "pluginId": "portfolio",
  "pluginName": "Portfolio",
  "githubUrl": "https://github.com/earnkeeper/ekp-portfolio",
  "ownerAddress": "0x7E5A9AAcA204d46A32072c3daD2E1fA427B5AF5F",
  "ownerChain": "bsc"
}
```

### Typescript

```typescript
socket.emit(
  "update-metadata",
  JSON.stringify({
    pluginId: "portfolio",
    pluginName: "Portfolio",
    githubUrl: "https://github.com/earnkeeper/ekp-portfolio",
    ownerAddress: "0x7E5A9AAcA204d46A32072c3daD2E1fA427B5AF5F",
    ownerChain: "bsc",
  })
);
```
