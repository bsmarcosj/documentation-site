{
  "title": "Peak traffic",
  "hideGithubLink": true,
	"pagetitle": "Alert type - Peak traffic",
  "description": "",
  "weight": 4,
  "icon": "fa-book",
  "alwaysopen": false
}

## Prupose

The purpose of this alert is to notify when there is some anomaly variation of traffic.

## Alert modes

### Standard

__comming soon!__

### Comparative

Este modo sirve para comparar el incremento o decremento de tráfico gracias a una cota superior e una cota inferior que son establecidas cada vez que se analiza la alerta. Estas cotas se calculan a partir del tráfico obtenido de la _historical\_window_ definida en la configuración de la alerta. A continuación encontraremos un ejemplo para ayudar a entender el funcionamiento de este modo, en dicho ejemplo la _historical\_window_ definida es de 20 minutos, el _offset_ es de 5 minutos y la _window_ es de 1 minuto. En dicho ejemplo podemos observar como a partir del minuto 18:15 se empieza a incumplir la alerta debido a que el tráfico pasa a estar por encima la cota superior.

{{< figure src="/images/alertsx_peak-traffic_comparative_en.svg#center" alt=" Four steps to using our API">}}

## Specific tags

### _historical\_window_
Tag for [comparative mode](#comparative)

Grandaria de la ventana pasada contra la que se compararar los datos actuales

### _offset_
Tag for [comparative mode](#comparative)

Desplazamiento de tiempo de la _historical\_window_ vs _window_
