# Add Layers

## Summary

This event is sent from the plugin to the front end app to add data to the client storage.

This data is in the form of documents, which are used to build the UI and store analytics data.

Check the Welcome page for more information.

## Specification

### Event Name

`add-layers`

### Event Fields

#### AddLayersEvent

| Fieldname | Type       | Description                            |
| --------- | ---------- | -------------------------------------- |
| layers    | LayerDto[] | List of layers to add to local storage |
| pluginId  | string     | Your unique plugin id                  |

#### LayerDto

| Fieldname      | Type          | Description                                                                                                     |
| -------------- | ------------- | --------------------------------------------------------------------------------------------------------------- |
| id             | string        | A unique id for this layer, can be used to refer to the layer later                                             |
| collectionName | string        | The name of the collection to add data to                                                                       |
| set            | DocumentDto[] | An array of documents to add to the collection. Existing documents with matching id will be overwrittern        |
| patch          | DocumentDto[] | An array of partial documents to update the collection with. Existing documents with matching id will be merged |

#### DocumentDto

| Fieldname | Type   | Description                                 |
| --------- | ------ | ------------------------------------------- |
| id        | string | The unique id of the document               |
| ...       | any    | Any further fields required by the document |

### Example

```json
{
  "pluginId": "portfolio",
  "layers": [
    {
      "id": "portfolio-token-balance-layer",
      "collectionName": "tokenBalances",
      "set": [
        {
          "id": "bnb-balance",
          "balanceFiat": 451.12,
          "balanceToken": 1,
          "chainId": "bsc",
          "tokenSymbol": "BNB",
          "tokenLogo": "https://cryptologos.cc/logos/thumbs/binance-coin.png?v=018"
        },
        {
          "id": "eth-balance",
          "balanceFiat": 1821.54,
          "balanceToken": 0.5,
          "tokenSymbol": "ETH",
          "chainId": "eth",
          "tokenLogo": "https://cryptologos.cc/logos/thumbs/ethereum.png?v=018"
        }
      ]
    }
  ]
}
```
