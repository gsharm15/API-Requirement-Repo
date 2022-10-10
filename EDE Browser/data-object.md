## Application Name : EDE Technical Browser

## Feature : Data Object

## 1. Data Object List

### UI Design

User would choose a context ID and data record type to land into a screen of data objects.

- Initially, user would be presented with the list of data objects available based on context and data record type selected.
  ![Data Objects List](https://user-images.githubusercontent.com/84699754/194290482-a921a697-a783-4654-aebc-48fabf82232b.png)

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
        "name": "", // not sure what dataRecord.name is
        "naturalKeyLabel": "",
        "primaryIdentitfier": "",
        "type": "",
        "filter": ""
      },
      "dataObject": {
        "name": "", // not sure what dataObject.name is
        "naturalKeyLabel": "",
        "primaryIdentitfier": ""
      }
    }
  ]
}
```

#### API Details

Endpoint for EDE browser not created yet

## 2. Data Object Metadata

### UI Design

- For each data object item is associated with metadata button. On click, the details should be presented as below.
  ![Metadata side sheet](https://user-images.githubusercontent.com/84699754/194297445-8398cbc1-0fd5-41c4-a57d-005fe30987a2.png)

### API Requirement

#### Proposed Response Schema

_Pagedata would contain paginated array of metadata properties._

```json
{
  "pageSize": 1,
  "pageIndex": 1,
  "totalRecords": 1,
  "totalPages": 1,
  "pageData": [
    {
      "id": "1",
      "primaryText": "Type",
      "secondaryText": "MTO S3D@HO"
    },
    {
      "id": "2",
      "primaryText": "Filter",
      "secondaryText": "{filter:X}"
    },
    {
      "id": "3",
      "primaryText": "Description",
      "secondaryText": "Description"
    }
  ]
}
```

#### API Details

Endpoint for EDE browser not created yet

Requirement : Based on primaryIdentitfier of the data object, the API should provide the metadata

## 3. Data Object Properties

### UI Design

- Each data object is associated with propeties which is classfied as "Property", "Feature" and "Relationship"
  ![Data Object Details](https://user-images.githubusercontent.com/84699754/194300278-cec0ccb1-872c-4604-b77c-feaf52040760.png)

### API Requirement

#### Proposed Response Schema

_Pagedata would contain paginated array of data objects_

Example response data:

```json
{
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
      "name": "", // not sure what dataRecord.name is
      "naturalKeyLabel": "",
      "primaryIdentitfier": "",
      "type": "",
      "filter": ""
    },
    "dataObject": {
      "name": "", // not sure what dataObject.name is
      "naturalKeyLabel": "",
      "primaryIdentitfier": ""
    },
  "propertyList": [
    {
      "name": "properties",
      "children": [
        {
          "id": "9a6c5313a1d44e5db163c2732c5f66f8",
          "canonicalPath": "employee.lastUpdatedDate",
          "programmaticName": "lastUpdatedDate",
          "displayName": "Last Updated Date",
          "value": "2",
          "unitOfMeasure": ""
        },
        {
          "id": "1",
          "canonicalPath": "employee.lastUpdatedDate",
          "programmaticName": "lastUpdatedDate",
          "displayName": "Date",
          "value": "00000000000000",
          "unitOfMeasure": ""
        },
        {
          "id": "2",
          "canonicalPath": "employee.lastUpdatedDate",
          "programmaticName": "lastUpdatedDate",
          "displayName": "New prop",
          "value": "222222222222222",
          "unitOfMeasure": ""
        }
      ]
    },
    {
      "name": "features",
      "children": [
        {
          "id": "425ecfe784ca42d08a4eb5bd502bdffd",
          "displayName": "Employee Pointer",
          "cardinality": "oneToOne",
          "value": {},
          "children": [
            {
              "id": "75cce1ff-fcbc-4b21-8bbc-c566af971d79",
              "canonicalPath": "employee.employeePointer.primaryIdentifier",
              "programmaticName": "primaryIdentifier",
              "displayName": "Primary Identifier",
              "value": "",
              "unitOfMeasure": "",
              "metadata": []
            },
            {
              "id": "af56b54c-c68d-47b1-b5ff-31539a7d8ee5",
              "displayName": "Object Identifier Label",
              "cardinality": "oneToOne",
              "value": {},
              "children": [],
              "metadata": []
            },
            {
              "id": "0b2e9ccf-bd06-4b29-9c2a-e7ab876be67d",
              "displayName": "Object Identifier Specification",
              "cardinality": "oneToOne",
              "value": {},
              "children": [],
              "metadata": []
            }
          ]
        },
        {
          "id": "5de1227621b74ecaadd2e035643aaeb1",
          "displayName": "Object Identifier",
          "cardinality": "oneToOne",
          "value": {},
          "children": [
            {
              "id": "067c2911-7b03-45f7-bb20-d600e9b02a0f",
              "canonicalPath": "employee.objectIdentifier.primaryIdentifier",
              "programmaticName": "primaryIdentifier",
              "displayName": "Primary Identifier",
              "value": "3a62c666db1341dbbb22502538318854",
              "unitOfMeasure": "",
              "metadata": []
            },
            {
              "id": "3bdd7886-fd40-4c7c-979b-ef6b64ca84bd",
              "displayName": "Object Identifier Label",
              "cardinality": "oneToOne",
              "value": {},
              "metadata": [],
              "children": [
                {
                  "id": "60a70b169587404db66d21388151ccd3",
                  "canonicalPath": "employee.objectIdentifier.objectIdentifierLabel.naturalKeyLabel",
                  "programmaticName": "naturalKeyLabel",
                  "displayName": "Natural Key Label",
                  "pn3": "objectIdentifier.objectIdentifierLabel.naturalKeyLabel",
                  "value": "",
                  "unitOfMeasure": "",
                  "metadata": []
                }
              ]
            },
            {
              "id": "a8fafe7a-d179-4074-8a80-44d16b0d9de7",
              "displayName": "Object Identifier Specification",
              "cardinality": "oneToOne",
              "value": {},
              "metadata": [],
              "children": [
                {
                  "id": "fb2ea6c1cf744638a32fd567a406c0d3",
                  "canonicalPath": "employee.objectIdentifier.employeeIdentitySpecification.designation",
                  "programmaticName": "designation",
                  "displayName": "Designation",
                  "pn3": "objectIdentifier.objectIdentifierSpecification.designation",
                  "value": 1208039550,
                  "unitOfMeasure": "",
                  "metadata": []
                }
              ]
            }
          ]
        }
      ]
    },
    {
      "name": "relationships",
      "children": [
        {
          "id": "425ecfe784ca42d08a4eb5bd502bdffd",
          "displayName": "Pipeline",
          "cardinality": "oneToOne",
          "value": {}
        },
        {
          "id": "425ecfe784ca42d08a4eb5bd502bdffd",
          "displayName": "Valve Connector",
          "cardinality": "oneToOne",
          "value": {}
        }
      ]
    }
  ]
}
```

#### API Details

Endpoint for EDE browser not created yet

Requirement : Based on primaryIdentitfier of the data object, the API should provide the properties
