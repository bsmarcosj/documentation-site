{
  "title": "Average time",
  "hideGithubLink": true,
  "pagetitle": "AlertsX - Average time",
  "description": "",
  "weight": 1,
  "icon": "fa-book",
  "alwaysopen": false
}

## Purpose

The main goal of this alert type is to detect anomalies related to the execution time of transactions. A usual configuration is to detect anomalies respect with the variation of average time percentage between windows.

## Alert modes

### Standard

Este modo tiene como objetivo avisar cuando el tiempo medio supera un tiempo previamente establecido. A continuación hay un ejemplo gráfico para hacer más comprensible este modo, en dicho ejemplo la _window_ de datos es de 5 minutos y el _max\_average_ configurado en la alerta es de 1 segundo:

{{< figure src="/images/alertsx_average-time_standard_en.svg#center" alt=" Four steps to using our API">}}

### Comparative

Este modo sirve para comparar el tiempo medio entre ventanas. Gracias a él podemos crear alertas que nos avisen si, por ejemplo, el tiempo medio actual se ha visto incrementado con respecto a un tiempo medio medido en un momento anterior. A continuación se enseña gráficamente del modo comparativo, en dicho ejemplo se ha configurado tanto la _window_ como la _historical\_window_ con un tamaño de 2 minutos, y un _offset_ de 3 minutos:

{{< figure src="/images/alertsx_average-time_comparative_en.svg#center" alt=" Four steps to using our API" attr="" >}}

En el ejemplo anterior se puede observar que el tiempo medio dentro de rango de la _historical\_window_ es de 883 milisegundos en cambio, dentro del rango de la _window_, claramente se ve que el tiempo medio llega a subir más de 1,25 segundos.

## Specific tags

### _max\_average_ (standard mode)

Tiempo límite por encima del cual la alerta saltará.

### _historical\_window_ (comparative mode)

Grandaria de la ventana pasada contra la que se compararar los datos actuales

### _offset_ (comparative mode)

Desplazamiento de tiempo de la _historical\_window_ vs _window_
