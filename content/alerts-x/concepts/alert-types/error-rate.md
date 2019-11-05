{
  "title": "Error rate",
  "hideGithubLink": true,
  "pagetitle": "Alert type - Error rate",
  "description": "",
  "weight": 2,
  "icon": "fa-book",
  "alwaysopen": false
}

## Purpose

The main goal of this alert type is to notify anomalies respect with the percentage of errors. By default, this alert type compares errors over the total but many more comparisons are possible.

## Alert modes

### Standard

Este modo tiene como objetivo avisar cuando el total de un conjunto de peticiones supera en "X"% al total de otro conjunto de peticiones dónde ambos conjuntos y "X" se definen en la configuración de la alerta. A continuación hay un ejemplo gráfico para hacer más comprensible este modo, en dicho ejemplo la _window_ de datos es de 1 minuto, el _percentage\_to\_alert_ está configurado al 50% y los campos _to\_check_ y _to\_compare_ se han dejado con su valor por defecto (peticiones erroneas contra el total de peticiones):

{{< figure src="/images/alertsx_error-rate_standard_en.svg#center" alt=" Four steps to using our API">}}

### Comparative

__comming soon!__

## Specific tags

### _to\_check_ ([standard mode](###Standard))

It's the appropiate tag in where desired error code/s to be reviewed must be set. By default this tag includes all wrong transactions.

### _to\_compare_ ([standard mode](###Standard))

It's the appropiate tag in where the error code/s to compare with must be set. By default this tag includes all transactions.

### _percentage\_to\_alert_ ([standard mode](###Standard))

ES: Porcentaje a partir del cual la alerta entrará en estado _alerting_. Dicho porcentaje es la ¿proporción/relación? entre el tráfico total del tipo de peticiones indicadas en el _to\_check_ y el tráfico total del tipo de peticiones indicadas en el _to\_compare_.

EN: Percentage when the alert will be triggered (Alerting state). This percentage is the relation between requests in to_check and requests in to_compare

### Possible comparisons

| Objective | to_check | to_compare |
| ------ | ------ | ------ |
| _default_ | empty (_all\_errors_) | empty (_all\_transactions_) |
| Integration errors VS Total transactions | 101 | empty (_all\_transactions_) |
| Integration errors VS Total errors | 101 | 101, 102, 104, 105, 204, 205, 206, 207, 301 |
| No availability VS Total OK | 204 | 0 |
