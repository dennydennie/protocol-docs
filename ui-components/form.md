# Form

JsonForms implementation for display of dynamic forms

<https://jsonforms.io/docs>

## Properties

| Name        | Type   | Description                                                      |
| ----------- | ------ | ---------------------------------------------------------------- |
| name\*      | string | The name of the form, used to store form results in client state |
| schema\*    | any    | The JsonForms Schema for the form                                |
| uischema\*  | any    | The JsonForms UI Schema for the form                             |
| submitLabel | string | Label to use for the submit button of the form, default "Save"   |

## Examples

### JSON

```json
{
    "_type": "Form"
}
```

### TypeScript

```javascript
Form({
  name: "critterzRentalCheck",
  uischema: {
    type: "Control",
    scope: "#/properties/tokenId",
    label: `Enter sCritterz Token ID`,
  },
  schema: {
    type: "object",
    properties: {
      tokenId: {
        type: "string",
      },
    },
    default: {
      tokenId: "",
    },
  },
  submitLabel: "Check",
});
```
