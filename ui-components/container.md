# Container

Powerful mobile-first flexbox grid to build layouts of all shapes and sizes thanks to a twelve column system, six default responsive tiers.

[https://reactstrap.github.io/?path=/docs/components-layout--layout](https://reactstrap.github.io/?path=/docs/components-layout--layout)

## See Also

{% content-ref url="card.md" %}
[card.md](card.md)
{% endcontent-ref %}

## Properties

| Name     | Type         | Description                                           |
| -------- | ------------ | ----------------------------------------------------- |
| children | UiElement\[] | The list of components to render inside the container |

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
