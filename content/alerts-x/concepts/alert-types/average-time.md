{
  "title": "Average time",
  "hideGithubLink": true,
  "pagetitle": "Alert type - Average time",
  "description": "",
  "weight": 1,
  "icon": "fa-book",
  "alwaysopen": false
}

## Purpose

The main goal of this alert type is to detect anomalies related to the execution time of transactions. A usual configuration is to detect anomalies respect with the variation of average time percentage between windows.

## Alert modes

### Standard
 
This mode aims to notify when the average time exceeds a previously established time. Below is a graphic example to make this mode more understandable, in that example the data _window_ is 5 minutes and the _max \ _average_ configured in the alert is 1 second:

{{< figure src="/images/alertsx_average-time_standard_en.svg#center" alt=" Four steps to using our API">}}

### Comparative

This mode is used to compare the average time between windows. Thanks to it, we can create alerts that let us know if, for example, the current average time has been increased compared to an average time measured at an earlier time. The following graphic shows the comparative mode, in this example both the _window_ and the _historical \ _window_ have been configured with a size of 2 minutes, and an _offset_ of 3 minutes:


{{< figure src="/images/alertsx_average-time_comparative_en.svg#center" alt=" Four steps to using our API" attr="" >}}

In the previous example can be seen that the average time within the range of the _historical \ _window_ is 883 milliseconds instead, within the range of the _window_, it is seen that the average time reaches more than 1.25 seconds.

## Specific tags

### _max\_average_ ([standard mode](###Standard))

Time limit above which the alert will notify of an alerting status.

### _historical\_window_ ([comparative mode](###Comparative))

Size of the last window against which the current window data is compared.

### _offset_ ([comparative mode](###Comparative))

Time from last minute of _historical\_window_ to last minute of _window_.