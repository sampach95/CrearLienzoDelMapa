# Crear Lienzo del Mapa
## Con las librerías previamente cargadas como lo vimos en el video correspondiente.

``` html
<html>
<head>
<meta charset="utf-8">
	<title>Mapa E14C17_2</title>
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.6.0/dist/leaflet.css"
  integrity="sha512-xwE/Az9zrjBIphAcBb3F6JVqxf46+CDLwfLMHloNu6KEQCAWi6HcDUbeOfBIptF7tcCzusKFjFw2yuvEpDL9wQ=="
  crossorigin=""/>
	<script src="https://unpkg.com/leaflet@1.6.0/dist/leaflet.js"
  integrity="sha512-gZwIG9x3wUXg2hdXF6+rVkLF/0Vi9U8D2Ntg4Ga5I5BZpVkVxlJWbSQtXPSiUTtC0TjtGOmxa1AJPuV0CPthew=="
  crossorigin=""></script>
```
 ## Continuamos abriendo una etiqueta style
    
``` html
	<style>
	#mapDIV {
	height: 100%;
	width: 100%;
	border: solid 2px black;
	}
	</style>
```

En ella declararemos el estilo del “lienzo del mapa”, utilizamos un selector de tipo identificador con la leyenda #mapDIV, seguimos por listar cada una de las propiedades de estilo que queremos que se visulicen.
Las propiedades Height y width: serán el ancho y el alto que ocupara el lienzo del mapa. El valor que toma puede estar expresado en px o porcentaje. En este caso el 100% indica que el lienzo del mapa ocupará toda la pantalla.
La propiedad border, agrega un marco alrededor del lienzo del mapa, el valor solid indica que se visualizará un color solido sin transparencias, el valor 2px indica el grosor del marco y el valor black es el color del marco.

## Cerramoss la etiqueta head, para iniciar a escribir el cuerpo de la pagina, para eso abrimos la etiqueta body, y acontinuacion usamos la etiqueta <div > para declarar que ahí se alojara nuestro mapa utilizando la instrucción “id”cerramos la etiqueta div.


``` html
</head>
<body>
<div id="mapDIV"></div>
 <script>
```
## Una vez creado el div, abrimos la etiqueta script que nos permite utilizar características de Java Script en páginas web.
Declaramos la variable map, después de la igualdad estará el contenido de la misma

``` javascript
     var map = L.map('mapDIV', {
		center:[17.8655, -99.8382],
		zoom:12
		});

```  
Primero” L.map”, la “L” hace referencia a la librería de Leaflet, se usa cada vez que vamos a utilizar una herramienta de la librería.

Separado por un punto se escribe map, que indica que vamos a trabajar en la visualización del lienzo del mapa, y nos permite hacer modificaciones a la forma en el que estará representado, en este caso, escribimos:

    Center, y entre corchetes, las coordenadas del centro de nuestro mapa, esto facilita la experiencia del usuario, ya que cuando abra la pagina del mapa este estará      situado en una ubicación geográfica determinada.
   
    Zoom, se utiliza para determinar cual será la vista inicial del mapa. Esta característica admite únicamente números enteros. 
    Si queremos que la visualización sea local el número será mayor, y para una visualización mas regional utilizamos un número menor -->
Cerramos todos los paréntesis y finalizamos con punto y coma

## Declaramos la variable scale, después de la igualdad estará en contenido de la misma.

``` javascript
var scale = L.control.scale({
	'imperial':false
	});
	
	scale.addTo(map);
```
Primero “L.control.scale”, que nos indica que haremos modificaciones en la escala gráfica del mapa
En este caso simplemente invalidaremos la escala gráfica en unidades del sistema inglés, de la siguiente forma ‘imperial’: false,
Cerramos corchetes y parentesís y finalizamos con punto y coma.
A continuación llamamos la variable “scale” y escribimos la instrucción “addTo” para agregar la escala grafica al mapa

Y por el momento, cerramos la etiqueta script, body y html

```html
 </script>
</body>
</html>
```
