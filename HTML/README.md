# TABLA DE CONTENIDO

[HTML](#html)

- [Anatomia de una pagina Web](#anatomia-de-una-pagina-web)
- [head](#head)
- [body](#body)
- [Anatomia de una etiqueta HTML](#anatomia-de-una-etiqueta-html)  

[Etiquetas Multimedia](#etiquetas-multimedia)  
  - [Tipos de Imagenes](#tipos-de-imagenes)  
  - [Optimizacion de imagenes](#optimizacion-de-imagen)  
  - [Etiqueta imagen](#etiqueta-imagen-img)  
  - [Etiqueta figure](#etiqueta-figure-y-figcaption)  
  - [Etiqueta video](#etiqueta-video)  

[FORMULARIOS](#formulario)  

# HTML

HTML significa Hypertext Markup Language que es un lenguaje de marcado de texto

## Anatomia de una pagina web

---

[Imagen de la anatomia de la web](https://escuelawow.com/anatomia-pagina-web-html/)

## HEAD

---

El primer archivo de **html** tiene que llamarse **index.html**

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="description" content="Esta página te mostrará fotos de gatos" />
    <meta name="robots" content="index,follow" />
    <title>Es mi página</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="./css/style.css" />
  </head>
  <body></body>
  <html></html>
</html>
```

**lang** : nos dice en que idiomae esta  
**meta** : Le dan cierta informacion al navegador para saber como se puede tratar el proyecto  
**title** : El titulo de la pagina

## BODY

---

El body son etiquetas contenedoras y van a ayudar a generar la estructura de la pagina

```html
<body>
  <header>
    <h1>Soy la lista del super!</h1>
  </header>
  <main>
    <ul>
      <li>Frutas</li>
      <ol>
        <li>Manzana</li>
        <li>Platano</li>
      </ol>
      <li>Carnes</li>
      <ol>
        <li>Pollo</li>
        <li>Carne molida</li>
      </ol>
      <li>Verduras</li>
      <ol>
        <li>Limón</li>
        <li>
          <a
            href="https://www.google.com/search?q=sopa+de+zanahoria&oq=sopa+de+zanah&aqs=chrome.0. 0l3j69i57j0l4.3060j0j7&sourceid=chrome&ie=UTF-8"
            >Zanahoria</a
          >
        </li>
      </ol>
    </ul>
  </main>
  <footer>
    <p>creado con amor</p>
  </footer>
</body>
```  
## Anatomia de una etiqueta html  
----  
 ``` html
 <a href:"https://youtube.com">Youtube</a>  
 ```  
 - Tiene una etiqueta de apertura y una de cierre  
 - Dentro de la etiqueta lleva el contenido  
 - a la etiqueta y al contenido se le llama elemento  
 - Lo que va dentro de la etiqueta se le llama atriburo  que tiene el nombre del atributo y el valor del atributo    

 # Etiquetas Multimedia  

 Son etiquetas para imagenes o videos  

 ## Tipos de Imagenes  
 ----  
  Lossiess (sin perdida)     
   -  Capturan todos los datos del archivo original  
   -  No se pierde nada del archivo original  
   -  Puede comprimirse pero podra reconstruir su imagen al estdo original 

  Lossy (con perdida): 
   - Se aproxima a su imagen original   
   - Podria reducir la cantidad de colores en su imagen o analizar la imagen en busca de datos innecesarios  
   - Por consiguiente puede reducir su tamaño, lo que mejora el tiempo de carga de la pagina pero pierde su calidad  
   - Los archivos tipo lossy son mucho mas liviano que los archivos tipo lossless por lo que son ideales para usar en sitios en donde el tamaño del archivo y la velocidad de descarga son importantes  

    TABLA DE DIFERENCIAS 
 
   |         | Categorias | Paleta          |   Uso                                                                          |
   |---------|------------|-----------------|--------------------------------------------------------------------------------|
   |  GIF    | Lossless        |max 256 colores      | animacion simple, graficar con colores planos                         |
   |  PNG-8  | Lossless        | max 256 colores     | sin animacion, ideal para iconos                                      |  
   |  PNG-24 | Lossless        | Colores ilimiados   | similar a png-8                                                       | 
   |  JPG    | Lossy           | Millones de colores | imagenes fijas, fotografias                                           |  
   |  SVG    | Vector/Lossless | Colores ilimitados  | graficos/logotipos para web,   retina/ pantalla de alta resolucion    |    

## Optimizacion de Imagen  
----
El tamaño optimo en promedio una imagen debe pesar al rededor de **70KB** y lo puedes hacer con   
 - **Tiny PNG** : mejora el tamaño de la imagen    
 - **Vereif** : retira metadatos de la imagen   

 ## Etiqueta imagen `<img/>` 
 ----
 ``` html 
 <img src="url/" alt="descripcion de la imagen" /> 
 ```

 ## Etiqueta `<figure>` y `<figcaption>`  
----
Es una etiqueta que permite almacenar una imagen en su interior, es una mejor practica comparada con usar solamente **div**  
`<figcaption>` permite darle una pequeña descripcion a la imagen como el autor, fuente o algo por el estilo   

``` html
<figure>
  <img src="./pics/tinifiel" alt="es una imagen de un gato"/>
  <figcaption>Es una imagen de un gato</figcaption>
</figures> 
```  
## Etiqueta `<video>`  
---- 
``` html 
<video src="./url" controls preload="auto"></video>
```  
`<sorce>` esta etiqueta nos deja poner un video con diferentes formatos  
``` html
<video  controls preload="auto">
  <source src="./url.m4v"/>
  <source src="./url.mp4"/>
</video>
```  

## FORMULARIO  
-----  
``` html 
<form action="">
  <label for="nombre">
    <span>Cual es tu nombre?</span>
    <input type="text" id="nombre" placeholder="tu nombre"></input>
  </label> 
  <label for="inicio-pregramacion">
    <span>Que dia comenzaste en platzi</span>
    <input type="text" id="inicio-programacion"></input>
  </label>
</form>
```  
## Calendario  
----
forma 1  
``` html
<form action="">
  <label for="hora">
    <span>Hora</span>
    <input type="time" id="hora" name="hora" />
  </label> 
  <label for="dia">
    <span>Día</span>
    <input type="date" id="dia" name="dia" />
  </label>
  <label for="semana">
    <span>Semana</span>
    <input type="week" id="semana" name="semana" />
  </label>
  <label for="mes">
    <span>Mes</span>
    <input type="month" id="mes" name="mes" />
  </label>
  <input type="submit">
</form>
```  
forma 2   
``` html
<form>
  <label for="calendario">
    <span>Calendario</span>
    <inputb type="datetime-local" id="calendario" name="calendario">
  </label>
  <input type="submit">
</form>
```  
[Clases de input](https://developer.mozilla.org/es/docs/Web/HTML/Element/input)  

## Autocomplete y require  
----- 

``` html 
<form action="">
  <label for="nombre">
    <span>Cual es tu nombre?</span>
    <input type="text" name="nombre" id="nombre" autocomplete="name">
  </label>

  <label for="correo">
    <span>Cual es tu correo electronico?</span>
    <input type="email" name="correo" id="correo" autocomplete="email">
  </label>

  <label for="pais">
    <span>En que pais vives?</span>
    <input type="text" name="pais" id="pais" autocomplete="country">
  </label>
  <input type="submit">
</form>
```

[Atributo autocomplete](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete)
