# Container

## Properties

| Name     | Type        | Description                                           |
| -------- | ----------- | ----------------------------------------------------- |
| children | UiElement[] | The list of components to render inside the container |

## Examples

### JSON

```json
{
  "_type": "Container",
  "props": {
    "children": [
      {
        "_type": "Row",
        "props": {
          "children": [
            {
              "_type": "Col",
              "props": [
                {
                  "children": [
                    {
                      "_type": "PageHeaderTitle",
                      "props": {
                        "title": "Rental Checker",
                        "icon": "cil-search"
                      }
                    }
                  ]
                }
              ]
            }
          ]
        }
      }
    ]
  }
}
```

### TypeScript

```ts
Container({
  children: [
    Row({
      children: [
        Col({
          children: [
            PageHeaderTile({
              title: "Rental Checker",
              icon: "cil-search",
            }),
          ],
        }),
      ],
    }),
  ],
});
```
