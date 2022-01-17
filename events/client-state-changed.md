# Client State Changed

## Summary

This event is sent from the front end app to the plugin whenever state changes due to user interaction.

It contains all information set by the user at the front end.

## Event Specification

### Event Name

`client-state-changed`

### Event Fields

#### ClientStateChangedEvent

| Fieldname | Type           | Description                               |
| --------- | -------------- | ----------------------------------------- |
| client    | ClientStateDto | Object containing the state at the client |

#### ClientStateDto

| Fieldname        | Type        | Description                                                |
| ---------------- | ----------- | ---------------------------------------------------------- |
| path             | string      | The relative path the user is browsing                     |
| selectedCurrency | CurrencyDto | The fiat currency selected by the user for display         |
| watchedChains    | string[]    | An array of chains the user has selected to view           |
| watchedWallets   | WalletDto[] | An array of wallet addresses the user has selected to view |

#### CurrencyDto

| Fieldname | Type   | Description                                            |
| --------- | ------ | ------------------------------------------------------ |
| id        | string | The id of the currency, matches CoinGecko currency ids |
| symbol    | string | The display symbol used to prefix currency values      |

#### WalletDto

| Fieldname | Type   | Description                                                 |
| --------- | ------ | ----------------------------------------------------------- |
| address   | string | The public address of the wallet, prefixed with 0x          |
| hidden    | string | Whether the user has chosen to hide this wallet temporarily |

## Example

```json
{
  "client": {
    "path": "portfolio/token/balances",
    "selectedCurrency": {
      "id": "usd",
      "symbol": "$"
    },
    "watchedChains": ["eth", "polygon", "bsc"],
    "watchedWallets": [
      {
        "address": "0x1a1ec25dc08e98e5e93f1104b5e5cdd298707d31",
        "hidden": false
      }
    ]
  }
}
```
