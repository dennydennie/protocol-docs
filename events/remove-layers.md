# Remove Layers

## Summary

Sent by the server to the client to remove layers from local storage when they are no longer needed or out of date.

## Specification

### RemoveLayersEvent

| Fieldname | Type            | Description                                            |
| --------- | --------------- | ------------------------------------------------------ |
| query     | LayerQueryDto[] | A query object defining which layers should be removed |
| pluginId  | string          | Your unique plugin id                                  |

### LayerQueryDto

| Fieldname | Type           | Description                                                                                                |
| --------- | -------------- | ---------------------------------------------------------------------------------------------------------- |
| id        | string         | The id of the layer to remove                                                                              |
| tags      | string[]       | An array of tags to search for layers to remove. Any layers with at least one matching tag will be removed |
| timestamp | NumberQueryDto | A query object to search for layers by timestamp                                                           |

### NumberQueryDto

| Fieldname | Type   | Description                                         |
| --------- | ------ | --------------------------------------------------- |
| eq        | number | Matches numbers equal to this value                 |
| gt        | number | Matches numbers greater than this value             |
| gte       | number | Matches numbers greater than or equal to this value |
| lt        | number | Matches numbers less than this value                |
| lte       | number | Matches numbers less than or equal to this value    |

## Example

```json
{
  "pluginId": "portfolio",
  "query": [
    {
      "id": "portfolio-token-balance-layer"
    }
  ]
}
```
