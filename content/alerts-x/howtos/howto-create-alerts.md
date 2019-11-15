{
"title": "Create Alert",
"pagetitle": "Create alert",
"description": "How to perform mutations on your alerts",
"icon": "fa-search-plus",
"weight": 4,
"alwaysopen": false,
"default_ak": "64780338-49c8-4439-7c7d-d03c2033b145",
"default_user": "",
"gists": [
    {
        "n":"Error rate 1",
        "g":"708148bb87432be5fbca20c0e5fd0f68",
        "o":["graphiql"],
        "u":"tgx-bot",
        "ak":"64780338-49c8-4439-7c7d-d03c2033b145"
    }, 
    {
        "n":"Error rate 2",
        "g":"4b07be538f151b2a75a184d22f26af9a",
        "o":["graphiql"],
        "u":"tgx-bot",
        "ak":"64780338-49c8-4439-7c7d-d03c2033b145"
    },
     {
        "n":"Average time 1",
        "g":"cce260c5bd43d2da1b252e89e7044967",
        "o":["graphiql"],
        "u":"tgx-bot",
        "ak":"64780338-49c8-4439-7c7d-d03c2033b145"
    }, 
     {
        "n":"Average time 2",
        "g":"67d52550bbe837e9021144cba561359b",
        "o":["graphiql"],
        "u":"tgx-bot",
        "ak":"64780338-49c8-4439-7c7d-d03c2033b145"
    }, 
     {
        "n":"Average time 3",
        "g":"694e031b53c6b4e5f83547b3eaa0629a",
        "o":["graphiql"],
        "u":"tgx-bot",
        "ak":"64780338-49c8-4439-7c7d-d03c2033b145"
    }, 
     {
        "n":"No traffic 1",
        "g":"af50aa4ff1c8534a88960d2fc2df76e5",
        "o":["graphiql"],
        "u":"tgx-bot",
        "ak":"64780338-49c8-4439-7c7d-d03c2033b145"
    },
    {
        "n":"Peak traffic 1",
        "g":"ec1edcea1e1427d83911223bf57654a6",
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

Alerts can be created in two ways. You can use our TravelgateX [API][website-API] or on our [website][website-alerts].

## Create an alert through TravelgateX API

To create an alert using TravelgateX API you must use the mutation `createAlert`. On the arguments of createAlert has to be set the input field. There are different configuration types in the input argument but only one can be set at the same time depending on the alert type you want to create.

In the schema of the API you can see mandatory(**!**) and optional fields but these those not means than optional fields do not need to be set. It depends on which mode of the alert type are you going to use. Alert types mode are explain [here][alerts-types]. If the configuration is not set correctly because has no all fileds needed or some value has no sense the API will response with an error. Posible errors are explained [here][].

Our complete TravelgateX API can be found [here][errors-types].

Below you will find some examples for different casuistry:  

| Mutation  |  Description |
|:-:|---|
| **Error rate 1**  |  `standard mode` using `time windowing`. (windowing modes explained [here][windowing-modes]) |
| **Error rate 2**| `standard mode` using `number of requests windowing`.|
| **Average time 1**| `comparative mode` using `time windowing`.|
| **Average time 2**| `standard mode` using `time windowing` and the specific tag `maximum average time`.|
| **Average time 3**| `standard mode` using `number of requests windowing` and the specific tag `maximum average time`.|  
| **No traffic 1**| `standard mode`  |
| **Peak traffic 1**| `comparative mode` using `time windowwing`.|

{{% graphiql-tabs %}}


{{% /graphiql-tabs %}}

{{< graphiql-styles >}}
{{% graphiql-script-tabs %}}


## Create an alert through TravelgateX website

An other way to create an Alert is doing directly on our website ("URL"). You can also found ir on the menu of Addons.

Steps:   

1. Select one of you folder which contains the product you want set the alert.  
2. Click on <span style="color:#c24413">**+ Create new**</span> bottom.  
3. **Conditions** : To Set Conditions first of all you must select an alert type.   
    - **Group** : You must select a product which the alert is going to check and set it as BUYER or SELLER.  

    -  **API** : You can select the API. (recommended)  

    - **Targets**: Used to filter the traffic you what to check with the alert. You can filter by suppliers, clients, accesses, hub status, operations, error codes and error types. there are two modes to filter, by _Inclusive_ or _Excludent_. Targets set as _Inclusive_ are options which are going to be checked. On the other     hand, if you set it has _Excludent_ all traffic is will be checked except the selected targets. Tagets selection is not mandatory, by default al traffic of the selected product will be checked.

    - **Agrupation** : This frame allows you to check the alert separetly for each combination of the agrupations selected. i.e.: If it is selected client & supplier you will receive the alerts of each combination client - supplier.  If agrupations are not selected the alert will check it with all traffic together.  
    
    - **Configuration** : This section is the only one that can change between the different alert types. Specific tags of each alert type will be in this frame. (Can see more details of specific tags here) There are also common tags:   
        - `periodicity`: frequency of time in minutes with which it is checked if the alert parameters are met.  

        - `window`: past minutes from now that are going to be checked.  

        - `times to alert`: the number of times (consecutive) the alert parameters must be accomplished to become <span style="color:#c24413">ALERTING</span> status and definitely send emails and change alert status as <span style="color:#c24413">ALERTING</span>.  

        - `times to recovery`: the number of times (consecutive) the alert parameters must be accomplished to become <span style="color:#00e37d">OK</span> status and definitely send emails and change alert status as <span style="color:#00e37d">OK</span>. 

        - `min number requests`: minimum number of requests must be in the window to check if the alert parameters are accomplished.
       
        - `percentage to alert`: the rate of traffic that has to acomplished the conditions of specific tags to be on ALERTING status.  

        - `no recoveries`: selected if you don't want to receive an email of status <span style="color:#00e37d">OK</span>.  

        - `state changes only`: select if you only want to receive an email when the alert status goes from <span style="color:#00e37d">OK</span> to <span style="color:#c24413">ALERTING</span> or vice versa. Ohterwise you wil receive an email each _periodicity_ time.  

4. **Notifications** : On this section has to be set almost one email which will receive the advise of <span style="color:#c24413">ALERTING</span> and <span style="color:#00e37d">OK</span> status. Using the _Add notification_ you will be able to set more emails as TO or BCC mails.  

5. **Description**: When email notification are sent, they'll include any text entered here. This can convey useful information about the problem and ways to approach fixing it.

6. **Name**: Here must be set a title for the alert. This makes easier to identify it quickly. This name also is going to be set in the subject of the email.  

7. Ones all previous sections have been filled only have to click on _Save_ to finish the process. If every think is correct you will see a green message to conrfirm the correct configuration.  
