# Poligonos
## Ahora que ya sabemos como se representan puntos y líneas, toca el turno a los polígonos. 
Estrictamente solo es un conjunto de líneas que al cerrarse representan un área.  Si te has dado cuenta, la información necesaria para representar cualquier geometría son coordenadas, los polígonos no son la excepción. A continuación, te mostramos el procedimiento básico. 
	
 ``` html
<script>	
 var polygon = L.polygon([[20.86114, -99.785305],[20.77543, -99.77069],[20.89791, -99.51015]], {color:'teal',weight:8}).addTo(map);
</script>
```
### Al ejecutar en tu navegador deberías tener algo como esto.

![screenshot](https://raw.githubusercontent.com/sampach95/Poligonos/master/img/poligonos.png )

Por defecto se cierra el polígono, utilizando los partes coordenados como vértices del triángulo en este caso, pero también se pueden representar otros polígonos como hexágonos y octágonos, por ejemplo. Otra cosa importante, es que por defecto se selecciona el mismo color de línea para el relleno del polígono esto lo podemos cambiar usando fillColor, y la opacidad con fillOpacity.

 ``` html
<script>	
  var polygon = L.polygon([[20.86114, -99.785305],[20.77543, -99.77069],[20.89791, -99.51015]], {color:'teal',weight:8, fillColor:'blue',fillOpacity:1}).addTo(map);
</script>
```
### Al ejecutar en tu navegador deberías tener algo como esto.

![screenshot](https://raw.githubusercontent.com/sampach95/Poligonos/master/img/poligonos2.png )

### Existen dos casos particulares que es necesario declaran utilizando otra clase diferente a “polygon”, son los rectángulos y lo círculos. A continuación, detallamos el procedimiento para cada uno.
#### RECTANGULOS
Para dibujar rectángulos utilizaremos la clase “L.rectangle()” y al igual que en los demás casos, usaremos pares coordenados para representar la figura, en particular para este caso solo son necesarias las coordenadas de las esquinas del rectángulo, a continuación te mostramos un ejemplo.

 ``` html
<script>	
  var rectangle = L.rectangle([[20.74625, -99.94663],[20.765841, -99.94882]], {color: "red", weight:8, fillColor:"blue"}).addTo(map);
</script>
```
### Al ejecutar en tu navegador deberías tener algo como esto.

![screenshot](https://raw.githubusercontent.com/sampach95/Poligonos/master/img/rectangulo.png )

##### CIRCULOS
Para trazar círculos utilizaremos la clase “L.cicle” y está vez utilizaremos un par coordenado y la medida en metros del radio que queremos representar.

Los polígonos nos pueden ser de gran utilidad para delimitar áreas de estudio o incluso realizar la cartografía geológica de una pequeña zona de estudio, siempre y cuando contemos con las coordenadas. 

``` html
<script>	
  	var circle = L.circle([20.89791, -99.51015], 10000,
		{color: "red",
		 weight:8,
		 fillColor:"blue"
		}
	).addTo(map);
</script>
```
### Al ejecutar en tu navegador deberías tener algo como esto.

![screenshot](https://raw.githubusercontent.com/sampach95/Poligonos/master/img/circulo.png )

Siguiente Tutorial https://github.com/sampach95/ObjetosMultiparte

Haz click en el siguiente enlace para volver a la pagina inicial
https://github.com/sampach95/ComoCrearMapasEnLaWebConLeaflet

