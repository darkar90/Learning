# Maquetacion de CSS

CSS significa **Cascading Style Sheet** hoja de estilo en cascada

- **Anatomia de una declaracion CSS: Selectro, Propiedades y Valores**

```css
* {
  background: papayawhip;
}
div {
  background: pink;
}
.titulo {
  color: blueviolet;
}
#titulo2 {
  color: brown;
}
a[href="https://platzi.com/home"]
{
  color: blue;
}
```

- **TIPOS DE SELECETORE**

  - **Selectores Basicos**
    - Selector **de Tipo** `div{}`
    ```css
    div {
      color: red;
    }
    ```
    - Selector **de Clase** `.elemento{}`
    ```css
    .elemnto {
      color: white;
    }
    ```
    - Selector **de ID** `#id-del-elemento{}`
    ```css
    #id {
      color: green;
    }
    ```
    - Selector **de Atributo** `a[href=""]{}`
    ```css
    a[href="https://youtube.com/home"]
    {
      color: pink;
    }
    ```
    - Selector **Universal** `*{}`
    ```css
    * {
      background: violet;
    }
    ```
  - **Selectores Combinadores**

    - Selector **Descendiente** `div p`

    ```css
    div p {
      color: red;
    }
    ```

    - Selector **Hijo directo** `div > p`

    ```css
    div > div {
      color: blue;
    }
    ```

    - Selector **Elemento Adyacente** `div + p`

    ```css
    div + section {
      color: pink;
    }
    ```

    - Selector **General de Hermanos** `div ~ p`

    ```css
    div ~ p {
      color: violet;
    }
    ```

    **Ejemplo**

    ```css
    <!DOCTYPE html>
    <html lang="en">
    <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div p {
        color: Lime;
        }
        div > div {
        background: plum;
        }
        .es {
        background: red;
        }
        div + section {
        background: palevioletred;
        }
        div ~ p {
        color: powderblue;
        }
    </style>
    </head>
    <body>
    <div>
        <div>
        <p>Platzi</p>
        <div class="es">Es</div>
        </div>
    </div>
    <p>Clase de selectores</p>
    <p>Clase de selectores</p>
    <section>
        Es lo mejor
    </section>
    <div>
        Master
    </div>
    </body>
    </html>
    ```

  - **PSEUDOCLASES**  
    Las Pseudoclases nos permiten llegar a aquellas acciones que hace el usurario  
     _ **:active**
    _ **:focus**
    _ **:hover**
    _ **:nth-chlid**
  - **PSEUDOELEMENTOS**  
    Son aquellos que nos permiten acceder a elementos de HTML que no son accesibles con otros selectores como por ejemplo la primera linea de un texto  
     _ **::after**  
     _ **::before**  
     _ **::first-letter**  
     _ **::placeholder**

  **Ejemplo**

  ```css
  <!DOCTYPE html>
  <html lang="en">
  <head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
      p {
      color: salmon;
      }
      p::first-letter {
      color: teal;
      }
      p::before {
      content: "✨";
      }
      p::after {
      content: "💅🏼";
      }
      p:hover {
      color: skyblue;
      }
      div p:nth-child(2) {
      color: violet;
      }
      ::placeholder {
      color: tomato;
      }
  </style>
  </head>
  <body>
  <p>Hola</p>
  <div>
      <p>Platzi</p>
      <p>Master</p>
      <p>Lo mejor</p>
  </div>
  <input type="text" placeholder="name">
  </body>
  </html>
  ```

  [Pseudo-Elemento-CSS-Documentacion](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)

  [Pseudo-Clases-Documentacio](https://css-tricks.com/pseudo-class-selectors/)

  - **ESPECIFICIDAD**  
    Quienes prevalecen sobre quienes  
     1. !important  
     2. Estilos en lines  
     3. #id  
     4. clases, atributos y Pseudoclases  
     5. Elementos y Pseudoelementos 6. Selectores Universales

  [Especifidad-calculadora](https://specificity.keegan.st/)

- **TIPO DE DISPLAYS**  
   Basicamente es el tipo de visualizacion que van a tener los elementos en HTML

  - **Block**  
     Estos elementos ocupan toda la pantalla
  - **Inline**  
     Estos elementos son los que su caja mide exactamente lo mismo que su contenido
  - **Inline-Block**  
     Esto es mezcla lo mejor de ambos, con este display se puede tener lo mejor de **Inline** como de **Block** es decir se visualiza como inline pero tiene caracteristicas de tipo block

  **Ejemplo**

  ```css
  <!DOCTYPE html>
  <html lang="en">
  <head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
      body {
      margin: 0;
      }
      div {
      background: salmon;
      width: 200px;
      height: 200px;
      margin: 20px;
      }
      a {
      background: skyblue;
      width: 200px;
      height: 200px;
      margin: 20px;
      }
      button {
      background: slateblue;
      width: 200px;
      height: 200px;
      }
  </style>
  </head>
  <body>
  <div>bloque</div>
  <a href="/">inline</a>
  <button>inline block</button>
  </body>
  </html>
  ```

  ***

  ***
