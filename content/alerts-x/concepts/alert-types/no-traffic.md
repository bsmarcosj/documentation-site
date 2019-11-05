{
  "title": "No traffic",
  "hideGithubLink": true,
	"pagetitle": "Alert type - No traffic",
  "description": "",
  "weight": 3,
  "icon": "fa-book",
  "alwaysopen": false
}

## Prupose

The main goal of this alert type is to notify when the total number of transactions is below a previously defined lowly bound.

## Alert modes

### Standard

Este modo tiene como objetivo detectar cuando el tráfico total disminuye por debajo de una cota inferior establecida. A continuación podemos encontrar un ejemplo gráfico para facilitar su comprensión, en dicho ejemplo la _window_ de datos es de 1 hora, y el _min\_number\_of\_requests_ (cota inferior) es de 65.000 transacciones, por lo que la alerta saltará cuando el tráfico total en una hora esté por debajo de esos 65k.

{{< figure src="/images/alertsx_no-traffic_standard_en.svg#center" alt=" Four steps to using our API">}}

### Comparative

__comming soon!__

## Specific tags

### _min\_number\_of\_requests_

Tag for [standard mode](#standard)

Campo común utilizado particularmente en este tipo de alerta para establecer la cota inferior a tener en cuenta a la hora de analizar la alerta.