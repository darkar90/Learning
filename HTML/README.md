# INICIO

[HTML](#html)  
[Etiquetas Multimedia](#etiquetas-multimedia)  
[Formularios](#formularios)

# HTML

[Maquetacion con HTML](#maquetacion)

**HTML** significa por sus siglas en ingles un **Lenguaje de Marcado de Texto** nos sirve para estructurar la pagina web

## Estructura Básica de HTML

---

- **Container:** contenedor principal
- **Header:** cabecera de la página. Aquí usualmente encuentras el logo y el menú de navegación del sitio.
- **Main content:** estructura principal. Por ejemplo, el feed o lista de publicaciones de una red social.
- **Sidebar:** contenido secundario de una página, que usualmente se encuentra a los lados del contenido principal (o main).
- **Footer:** pie de página. Esto se encuentra al fondo del sitio web, salvo en casos de sitios web donde el scroll (o navegación hacia abajo) es infinito, por ende, no tendría sentido ponerlo al fondo.

## Estructura Básica de HEAD

---

```html
<head>
  <meta charset="UTF-8" />
  <meta name="description" content="Esta página te mostrará fotos de gatos" />
  <meta name="robots" content="index,follow" />
  <title>Es mi página</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="./css/style.css" />
</head>
```

## Estructura Básica Body

---

- Etiqutas del cuerpo del documento (body)

  - **article:** diferencia partes del contenido que pueden vivir por sí mismas.
  - **nav:** para hacer menús de navegación.
  - **aside:** contenido menos relevante, como publicidad, etc.
  - **section:** sirve para diferenciar las secciones principales del contenido.
  - **header:** cabecera del documento.
  - **footer:** pie de página del documento.
  - **h1 - h6:** títulos de nuestro sitio web.
  - **table:** tablas de contenidos, similar a la estructura de las hojas de calculo.
  - **ul y ol:** listas de items.
  - **div:** cualquier división para organizar el contenido.
  - **h1 a h6:** son etiquetas para indicar títulos con un estilo que destaca del resto.
  - **article:** es la parte de nuestro contenido que puede vivir por sí mismo. Pueden haber tantos artícle como proyectos o eventos tenga nuestro portafolio.
  - **p:** define el texto de un párrafo.
  - **small:** aplica una apariencia de texto reducido en tamaño.
  - **strong:** aplica al texto un formato de negritas.
  - **a:** corresponde a un ancla o enlace a una url interna o externa del documento.
  - **img:** con esta etiqueta podemos enlazar imágenes en el documento.
  - **figure:** le da un contexto semántico a las imágenes.

  ```html
  <body>
    <header>
      <!--Sección superior de nuestro website-->

      <nav></nav>
      <!--Sección de navegación de nuestro website, siempre dentro del header-->
    </header>

    <main>
      <!--Main es el contenido central de nuestro website, "la parte del medio"-->

      <section>
        <!--Nuestro website puede estar divido por secciones, por ejemplo platzi tiene 3: El navegador de cursos y rutas, el feed y nuestras rutas de aprendizaje-->

        <article>
          <!--Contenido independiente de la página. Es reutilizable-->
        </article>
      </section>

      <ul>
        <!--Lista desordenada: Sin numerar-->

        <li><!--Item List. Elementos de la lista--></li>
      </ul>

      <ol></ol>
      <!--Lista ordenada: Numerada-->
    </main>

    <footer><!--Sección final de nuestro website--></footer>

    <p>Soy un texto</p>
    <!--Párrafo, texto-->

    <h1>Soy un titulo</h1>
    <!--Títulos, muestran el texto más grande y con negrilla. Existen desde el h1 al h6-->

    <a href="#">Soy un link</a>
    <!--Enlaces/links que nos permitirán movernos entre páginas.-->
  </body>
  ```

## ETIQUETAS MULTIMEDIA

---

- **Tipos de Imagenes**

  - **Lossless (sin pérdida)**

    - Capturan todos los datos del archivo original.
    - No se pierde nada del archivo original.
    - Puede comprimirse, pero podrá reconstruir su imagen al estado original

  - **Lossy (con pérdida)**

    - Se aproximan a su imagen original.
    - Podría reducir la cantidad de colores en su imagen o analizar la imagen en busca de datos innecesarios.
    - Por consiguiente puede reducir su tamaño, lo que mejora el tiempo de carga de la página, pero pierde su calidad.
    - Los archivos tipo lossy son mucho más livianos que los archivos tipo lossless, por lo que son ideales para usar en sitios en donde el tamaño del archivo y la velocidad de descarga son importantes.

- **Fromato de Imagen para Web**

  - **GIF (Graphics Interchange Format):** Formato de imagen sin pérdida, no se puede comprimir
  - **PNG 8 (Portable Network Graphics):** Formato de imagen sin pérdida, uso de colores de 256, se utiliza para logotipos e iconos para la página.
  - **PNG 24 (Portable Network Graphics):** Formato de imagen sin pérdida, utilización de colores ilimitados, alta calidad, si intentamos comprimir no ayudará demasiado por la gran cantidad de colores.
  - **JPG / JPEG (Photographic Experts Group):** Formato de imagen con pérdida, perdemos calidad a la hora de comprimirlas, pero llegan a ser óptimas para la carga en la página web.
  - **SVG - Vector (Scalable Vector Graphics):** Formato de imagen muy ligero sin pérdida, con svg no perdemos calidad, ya que está compuesta por vectores.
  - **WebP:** Es un formato gráfico en forma de contenedor que sustenta tanto compresión con pérdida como sin ella. ​​Fue desarrollado por Google.

- **Figure y Img**  
  Figure es una etiqueta que permite almacenar una imagen en su interior es una mejor practica semanticamente hablando que usar la etiqueta **div**

  **Figcaption** se diferencia del atributo Alt porque esta última muestra su descripción en texto en el navegador solamente al pasar el mouse por encima de la imagen (de ahí su utilidad para personas con discapacidad visual).

  ```html
  <figure>
    <img src="./pics/tinified/small.jpg" alt="Es una imagen de un perrito" />
    <figcaption>Es una imagen de un perrito</figcaption>
  </figure>
  ```

- **Etiquta Video**  
  La etiqueta <video>, tiene algunos atributos como:

  - **controls:** agrega al video los controles necesarios para reproducir, pausar y adelantar.

  - **preload = auto:** hace que el navegador descargue el video, en el momento en el que se acceda a la página.

  La etiqueta <source>, se puede colocar dentro de una etiqueta <video> varias veces, para especificar diferentes rutas. Esto para asegurar que cualquier navegador pueda mostrar el video.

  ```html
  <body>
    <main>
      <section>
        <video controls preload="auto">
          <source src="./Episodio4.m4v#t=10,60" />
          <source src="./Episodio4.mp4#t=10,60" />
        </video>
      </section>
    </main>
  </body>
  ```

## **Formularios**

---

[Elementos de formulario](https://www.w3schools.com/html/html_form_input_types.asp)

```html
<body>
  <form action="">
    <label for="nombre">
      <span>¿Cual es tu nombre?</span>
      <input type="text" id="nombre" placeholder="Tu nombre" />
    </label>
    <label for="inicio-platzi">
      <span>¿Qué día comenzaste en Platzi?</span>
      <input type="date" id="inicio-platzi" />
    </label>
    <label for="horario">
      <span>¿En que horario estudias?</span>
      <input type="time" id="horario" />
    </label>
  </form>
</body>
```

## MAQUETACION

---

- **Anatomia de un documento HTML**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <p>primer parrafo</p>
    <ol>
      <li>uno</li>
      <li>dos</li>
    </ol>
  </body>
</html>
```

- **Atributos**  
  Tambien se puede colocar atributos

```html
<p class="title">prueba</p>
<p>
  <!--atributo = valor-->
</p>
```

- **HTML Semantico**
  - Ayuda al sitio a ser accesible
  - Mejora posicionamiento en CEO
  - Código mas claro

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <header></header>
    <nav>
      <ul></ul>
    </nav>

    <footer></footer>
  </body>
</html>
```

- **Etiquetas de HTML mas usadas**

  - Layout

  ```html
  <header></header>
  <nav></nav>
  <section></section>
  <article></article>
  <aside></aside>
  <footer></footer>
  ```

  - Textos

  ```html
  <h1></h1>
  <h2></h2>
  <h3></h3>
  <h4></h4>
  <h5></h5>
  <h6></h6>
  <p></p>
  <span></span>
  ```

  - Imagenes y Videos

  ```html
  <img />
  <svg>
    <iframe>
      <video></video>
    </iframe>
  </svg>
  ```

  - Formularios

  ```html
  <form></form>
  <input />
  <label> <button></button></label>
  ```

  - Listas

  ```html
  <ul></ul>
  <li></li>
  <ol></ol>
  ```

  - Enlaces

  ```
  <a></a>
  ```

  **Ejemplo**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <nav>
      <ul>
        <li>about us</li>
        <li>contact us</li>
      </ul>
    </nav>
    <section>
      <div>
        <img
          src="https://images.pexels.com/photos/1741205/pexels-photo-1741205.jpeg?auto=compress&cs=tinysrgb&h=650&w=940"
          alt="cat"
        />
      </div>
      <div>
        <h1>Cats</h1>
        <p>Cats are awesome</p>
      </div>
    </section>
    <form action="">
      <label for="name">Name</label>
      <input type="text" id="name" />
    </form>
    <a href="https://platzi.com/home">Go to Platzi</a>
  </body>
</html>
```
