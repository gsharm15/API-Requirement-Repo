## Feature : Data Record

## 1. Data Record List

### UI Design

User would choose a context ID and data record type to land into a screen of data objects.

- Initially, user would be presented with the list of data Recirds available based on multiple context selected.
- ![image](https://user-images.githubusercontent.com/99733969/194864304-69a48c47-9288-4809-b47d-cb430b40bc62.png)


### API Requirement

#### Proposed Response Schema

_Pagedata would contain paginated array of data objects_

```json
{
  "pageSize": 1,
  "pageIndex": 1,
  "totalRecords": 1,
  "totalPages": 1,
  "pageData": [
    {
      "context": {
        "id": "73245dfe2bf2461a94015a2f4c46f7c8",
        "name": "97624-100",
        "description": "97624-100, - UAT Development, Configuration in UAT (For ACNX Data flows)"
      },
      "entity": {
        "name": "Valve"
      },
      "dataRecord": {
        "naturalKeyLabel": "",
        "primaryIdentitfier": "",
        "type": "",
        "filter": "",
        "dataRecordType":"type + filter"
      },
      "dataObject": {
        "naturalKeyLabel": "",
        "primaryIdentitfier": ""
      }
    }
  ]
}
```

#### API Details

Endpoint for EDE browser not created yet

