{
  "title": "AlertsXQuery",
  "description": "",
  "weight": 1,
  "fields": [
    {
      "typeString": "AlertConnection!",
      "name": "alerts",
      "url": "/alerts-x/api-reference/objects/alertconnection",
      "description": "Query to obtain Alerts",
      "isDeprecated": false,
      "args": [
        {
          "typeString": "RelayInput",
          "name": "relay",
          "url": "/alerts-x/api-reference/inputobjects/relayinput",
          "description": null
        },
        {
          "typeString": "AlertFilterInput",
          "name": "filter",
          "url": "/alerts-x/api-reference/inputobjects/alertfilterinput",
          "description": null
        },
        {
          "typeString": "AlertCriteriaInput!",
          "name": "criteria",
          "url": "/alerts-x/api-reference/inputobjects/alertcriteriainput",
          "description": null
        }
      ]
    }
  ],
  "requireby": null,
  "enumValues": null,
  "operator": "type",
  "typename": "AlertsXQuery",
  "hideGithubLink": true
}
## GraphQL schema definition

{{% graphql-schema-type %}}

## Fields

{{% graphql-field %}}
