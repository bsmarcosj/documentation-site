{
  "title": "SystemData",
  "description": "",
  "weight": 1,
  "fields": [
    {
      "typeString": "ID!",
      "name": "code",
      "url": "/stats/reference/scalars/id",
      "description": null,
      "isDeprecated": false,
      "args": null
    },
    {
      "typeString": "ID!",
      "name": "name",
      "url": "/stats/reference/scalars/id",
      "description": null,
      "isDeprecated": false,
      "args": null
    },
    {
      "typeString": "Boolean!",
      "name": "isActive",
      "url": "/stats/reference/scalars/boolean",
      "description": null,
      "isDeprecated": false,
      "args": null
    },
    {
      "typeString": "Group",
      "name": "group",
      "url": "/stats/reference/objects/group",
      "description": null,
      "isDeprecated": false,
      "args": null
    },
    {
      "typeString": "Organization",
      "name": "owner",
      "url": "/stats/reference/objects/organization",
      "description": null,
      "isDeprecated": false,
      "args": null
    },
    {
      "typeString": "[Supplier]!",
      "name": "suppliers",
      "url": "/stats/reference/objects/supplier",
      "description": null,
      "isDeprecated": false,
      "args": [
        {
          "typeString": "SupplierFilter",
          "name": "filter",
          "url": "/stats/reference/inputobjects/supplierfilter",
          "description": null
        }
      ]
    }
  ],
  "requireby": [
    {
      "name": "System",
      "description": null,
      "url": "/stats/reference/objects/system"
    }
  ],
  "enumValues": null,
  "operator": "type",
  "typename": "SystemData",
  "hideGithubLink": true
}
## GraphQL schema definition

{{% graphql-schema-type %}}

## Fields

{{% graphql-field %}}

## Required by

{{% graphql-require-by %}}
