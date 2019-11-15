{
  "title": "Window modes",
  "hideGithubLink": true,
  "pagetitle": "AlertsX - Windowing",
  "description": "",
  "weight": 2,
  "icon": "fa-book",
  "alwaysopen": false
}

## Contexto

El tráfico que se mueve en TravelgateX es no es algo finito debido al constante flujo de peticiones que llegan a sus sitemas, es debido a esto que se necesitan crear subconjuntos virtuales finitos de este conjunto en expansión, formado por el tráfico total, para así poder analizarlo de forma correcta. Esto se aplica a **todos** los tipos de alertas.

{{< figure src="/images/alertsx_windowing_1_es.jpg#center" alt=" Four steps to using our API" attr="" >}}

## Subconjuntos finitos de datos

AlertsX permite configurar dos formas distintas de que se formen dichos subconjuntos finitos. La primera consiste en establecer ventanas temporales gracias a las cuáles AlertsX irá creando dichos conjuntos de datos, i.e. una ventana de datos de 1 minuto creara un conjunto de datos virtual cada mínuto que acojerá a todas las transacciones ejecutadas en dicho minuto. Para la segunda únicamente se debe decidir el tamaño que tienen que tener los subconjuntos creados, el subconjunto se creará y se le irán añadiendo datos hasta que estén lleno y cuando eso pase, se analizará y se irá creando otro subconjunto.

### Alerta por ventana temporal

Para que la alerta utilice ventanas temporales, el usuario únicamente se tiene que decidir cuál debe ser el intervalo de tiempo que se va a utilizar para para comprobar si se cumplen o no las reglas que la alerta tiene configuradas. Si por ejemplo, el usuario configura la alerta con una "window" de 5 minutos, cada vez que se vaya a comprobar la alerta se tendrán en cuenta todas las transacciones transcurridas en los últimos 5 minutos.

### Alerta por cantidad de peticiones

Cuando hablamos de ventanas por cantidad de peticiones, se tiene que ser consciente de que la alerta puede no comprobarse en periodos de tiempos iguales. Al establecer que, por ejemplo, las ventanas se creen de exactamente 1000 elementos, se le está diciendo a la alerta que hasta que no hayamos recopilado esos 1000 elementos no debe comprobar las reglas que tiene configurada. Puede darse el caso de que en un momento dado haya pasado únicamente un minuto y ya se tengan los 1000 elementos para poder evaluar la alerta, pero también podría darse el caso de que habiendo pasado 1 minuto no se haya llegado a los elementos necesarios, por lo que la alerta debería esperar más tiempo para empezar la evaluación de sus reglas.
