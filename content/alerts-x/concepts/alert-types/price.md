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

### Undividual

In this mode the alert will be triggered if at least one transaction does not accomplish the rules set.

### Percentage

In this mode the alert will be triggered when certain percentage of transaccions do not accomplish the rules set. This percentage is configured in the tag _percentage\_to\_alert_

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
