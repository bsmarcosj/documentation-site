{
  "title": "Error rate",
  "hideGithubLink": true,
  "pagetitle": "AlertsX - Error rate",
  "description": "",
  "weight": 2,
  "icon": "fa-book",
  "alwaysopen": false
}

## Purpose
The main goal of this alert type is to notify anomalies respect with the percentage of errors. By default, this alert type compares errors over the total but many more comparisons are possible.

## Alert modes
### Standard
Este modo tiene como objetivo avisar cuando el total de un conjunto de peticiones supera en X al total de otro conjunto de peticiones dónde ambos conjunto y X se definen en la configuración de la alerta.

### Comparative (comming soon!)

## Specific tags
### _to\_check_
It's the appropiate tag in where desired error code/s to be reviewed must be set.

### _to\_compare_
It's the appropiate tag in where the error code/s to compare with must be set.

### Possible comparisons
| Objective | to_check | to_compare |
| ------ | ------ | ------ |
| _default_ | empty (_all\_errors_) | empty (_all\_transactions_) |
| Integration errors VS Total transactions | 101 | empty (_all\_transactions_) |
| Integration errors VS Total errors | 101 | 101, 102, 104, 105, 204, 205, 206, 207, 301 |
| No availability VS Total OK | 204 | 0 |