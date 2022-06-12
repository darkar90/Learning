# HTML

[Maquetacion con HTML](#maquetacion)

**HTML** significa por sus siglas en ingles un **Lenguaje de Marcado de Texto** nos sirve para estructurar la pagina web

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

La anatomia de un documento de HTML tiene una etiqueta de apertura y una etiqueta de salida con el contenido adentro

```html
<h1>
  pruba
  <h1></h1>
</h1>
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
