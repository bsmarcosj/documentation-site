{
  "title": "Price",
  "hideGithubLink": true,
  "pagetitle": "Alert type - Price",
  "description": "",
  "weight": 5,
  "icon": "fa-book",
  "alwaysopen": false
}

## Prupose

The purpose of this alert is to notify when is some anomaly variation of pricing. This is only available for hotel API.

API: Hotel

Method: Quote

## Alert modes

### Unit

An alert will be sent for each transaction that does not accomplish the values set (amount/commission)

### Percentage

An alert will be sent if percentage_to_alert is accomplished.

## Specific tags

### _amount_

The amount set must be in €

### _commission_

The commission set must be in %

### _check_

To set what do you want to check, amount, commission or both.

Values:

* amount
* commission
* all

### _range_

Values:

* less
* greater

### _amount\_by_

Amount value can be by night or total.

Values:

* night
* total
