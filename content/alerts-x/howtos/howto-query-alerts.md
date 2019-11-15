{
"title": "Query Alerts",
"pagetitle": "Query alerts",
"description": "How to query about your alerts",
"icon": "fa-search-plus",
"weight": 4,
"alwaysopen": false,
"default_ak": "64780338-49c8-4439-7c7d-d03c2033b145",
"default_user": "",
"gists": [
    {
        "n":"location group",
        "g":"d68e218b7d2039d35b6b7d8ef58131d1",
        "o":["graphiql"],
        "u":"tgx-bot",
        "ak":"64780338-49c8-4439-7c7d-d03c2033b145"
    }, 
    {
        "n":"alert code",
        "g":"b6d2360840706de09b0c306ebdcbdc21",
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

Alerts can be retrieved in two ways. You can use our TravelgateX [API][website-API] or on our [website][website-alerts].

## Retrieve alerts by TravelgateX API

To retrieve alerts allready exist in you organization using TravelgateX API you must use the query `alerts`. On the arguments of `alerts` can be used to filter alerts returned.   
The `Arguments` are explained bellow:  

- criteria:  
    - `alertCodes`: can set a list of alert codes allready known. i.e.: `ALT_210`
    - `groups`: can set a list of group codes allready known. i.e.: `AlertsX_11805`
    - `isActive`: boolean to get active or no active alerts.
    - `shared`: common alerts are private of each organization, but also can be set alerts to be viewed by all users of travelgateX. To get only alerts from you organizations set `GROUP`.  To get alerts shared with all users set `TGX`.

Our complete TravelgateX API can be found [here][schema].

Below you will find some examples for different casuistry and its description.

| Query  |  Description |
|:-:|---|
| **Group location**  |  Get alerts `located` in the group/s indicated|
| **Alert code**| Get `specific` alerts by its code  |
| **Without criteria**| Get `all` alerts you can read |

{{% graphiql-tabs %}}


{{% /graphiql-tabs %}}

{{< graphiql-styles >}}
{{% graphiql-script-tabs %}}

## Create an alert through TravelgateX website

An other way to retrieve Alerts is doing directly on our [website][website-alerts]. You can also found it on the menu of Addons.
 
1. Select one of you folder which contains the alerts. Ones selected you will get all alerts corresponding to the products of the folder selected.
2. You can check the `last 10 states` of an alerts (or agrupation of alerts) by doing click on the eye/arrow symbol to the left of each alert.
3. You also can check if the alert is active or not by the switch checkbox. If its <span style="color:#0088DD">blue</span> it means the alert is active and it is desactivate if it's <span style="color:#DEE2E6">grey</span>.
