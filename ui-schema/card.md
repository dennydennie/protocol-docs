# Card

## Properties

| Name     | Type        | Description                                       |
| -------- | ----------- | ------------------------------------------------- |
| title    | string      | The card title                                    |
| children | UiElement[] | The list of components to render in the card body |

## Examples

### JSON

```json
{
  "_type": "Card",
  "props": {
    "title": "An example title",
    "children": [
      {
        "_type": "Span",
        "props": {
          "content": "An example body"
        }
      }
    ]
  }
}
```

### TypeScript

```ts
Card({
  title: "Example title",
  children: [Span({ content: "An Example Body" })],
});
```
