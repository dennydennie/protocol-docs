# Datatable

React datatable with sorting, expandable rows and pagination.

<https://react-data-table-component.netlify.app/>

columns: DatatableColumn[];
data: RpcOrPrimitive;
defaultSortAsc?: RpcOrPrimitive;
defaultSortFieldId?: RpcOrPrimitive;
pagination?: RpcOrPrimitive;
paginationPerPage?: RpcOrPrimitive;
onRowClicked?: Rpc;

## Supported Properties

EarnKeeper does not support all properties of the underlying control, the currently supported properties are below.

| Name               | Type               | Description                                                                                                               |
| ------------------ | ------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| columns\*          | DatatableColumn\[] | The list of column definitions to use for the table, see below for the specification                                      |
| data\*             | Rpc\|any[]         | The data to display in the table, as a reference to locally stored data, see the Data Specification section for more info |
| defaultSortAsc     | Rpc\|boolean       | Set this to false if you want the table data to be sorted in DESC order.                                                  |
| defaultSortFieldId | Rpc\|string        | Sets the a column to be pre sorted and corresponds to the a column definition id.                                         |
| pagination         | Rpc\|boolean       | Enable pagination with defaults.                                                                                          |
| paginationPerPage  | Rpc\|number        | The default rows per page to use when the table initially loads.                                                          |
| onRowClicked       | Rpc                | Rpc to run when a row is clicked                                                                                          |

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

```javascript
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
