## Feature : Data Record

## 1. Data Record List

### UI Design

User would choose a context ID to land into a screen of data Records.

- Initially, user would be presented with the list of data Recirds available based on multiple context selected.
- ![image](https://user-images.githubusercontent.com/99733969/194864304-69a48c47-9288-4809-b47d-cb430b40bc62.png)


### API Requirement

#### Proposed Response Schema

_Pagedata would contain paginated array of data records_

```json
[
    {
        "pageSize": 1,
        "pageIndex": 1,
        "totalRecords": 1,
        "totalPages": 1,
        "context": {
            "id": "73245dfe2bf2461a94015a2f4c46f7c8",
            "name": "97624-100",
            "description": "97624-100, - UAT Development, Configuration in UAT (For ACNX Data flows)"
        },
        "pageData": [
            {
                "naturalKeyLabel": "",
                "primaryIdentitfier": "",
                "type": "",
                "filter": ""
            },
            {
                "naturalKeyLabel": "",
                "primaryIdentitfier": "",
                "type": "",
                "filter": ""
            }
        ]
    },
    {
        "pageSize": 1,
        "pageIndex": 1,
        "totalRecords": 1,
        "totalPages": 1,
        "context": {
            "id": "12345dfe2bf2461a94015a2f4c46f767",
            "name": "26173-777",
            "description": "26173-777, - DEV Development, Configuration in DEV (For ACNX Data flows)"
        },
        "pageData": [
            {
                "naturalKeyLabel": "",
                "primaryIdentitfier": "",
                "type": "",
                "filter": ""
            },
            {
                "naturalKeyLabel": "",
                "primaryIdentitfier": "",
                "type": "",
                "filter": ""
            }
        ]
    }
]```

#### API Details

Endpoint for EDE browser not created yet

