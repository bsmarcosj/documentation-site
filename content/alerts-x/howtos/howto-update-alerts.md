{
"title": "Update Alert",
"pagetitle": "Alert - Update",
"description": "How to update your alerts",
"icon": "fa-search-plus",
"weight": 4,
"alwaysopen": false,
"default_ak": "64780338-49c8-4439-7c7d-d03c2033b145",
"default_user": "",
"gists": [
    {
        "n":"windows update",
        "g":"0536613ed120dac66dd14cefcec85921",
        "o":["graphiql"],
        "u":"tgx-bot",
        "ak":"64780338-49c8-4439-7c7d-d03c2033b145"
    }
    ]
}

[website-API]: https://api.travelgatex.com/
[website-alerts]: https://www.travelgatex.com/alerts
[alerts-types]: /alerts-x/concepts/alert-types
[noTraffic-type]: /alerts-x/concepts/alert-types/no-traffic
[errors-types]: /alerts-x/
[windowing-modes]: /alerts-x/concepts/windowing-modes
[schema]: /alerts-x/api-reference

Alerts can be updated in two ways. You can use our TravelgateX [API][website-API] or our [website][website-alerts].

## Retrieve alerts by TravelgateX API

To retrieve alerts allready exist in you organization using TravelgateX API you must use the mutation `updateAlert`. The arguments of `updateAlert` are mandatory.
The `Arguments` are explained bellow:  

- criteria:
    - `code`: must the alert code you want to update. i.e.: `ALT_210`
    - `input`: to do the settings changes you want. As the create process you have to select only one alert type configuration. Is not necessary to set all the alert parameters. You only need to set the parameter you have to change, the other one will be the same if it's there no input of the parameter. 

Our complete TravelgateX API can be found [here][schema].

Below you will find some examples for different casuistry and its description.

| Query  |  Description |
|:-:|---|
| **Window update**  |  Update the `window` parameter of a `no traffic` alert type. If previously was not a no traffic alert type it would be changed.|
| **Email update** | Update the `emails` where have to be send de OK & ALERTING advises. |


{{% graphiql-tabs %}}


{{% /graphiql-tabs %}}

{{< graphiql-styles >}}
{{% graphiql-script-tabs %}}

## Create an alert through TravelgateX website

An other way to update an alert is doing it directly on our [website][website-alerts]. You can also found it on the menu of Addons.
 
 Steps:

1. Select one of you folder which contains the alerts. Ones selected you will get all alerts corresponding to the products of the folder selected.
2. You have to click on the menu (three dots) found on the right of the alert row (last column ``Actions``). On the menu will appear the option ``Edit``, click it.
3. Ones clicked on Edit button it will appears the same page you get to create an alert but with all parameters setted.
4. Change one or many parameters you need and finished by doing click on ``Save`` button located at the bottom of the page.
5. If it is everything correct the alert will be successful and alert would be updated. You can check the posible errors returned [here][errors-types]

WARNING: historical status will be deleted automatically. Exception: status will not be deleted if parameters updated are ``name``, ``description`` or ``email``.

