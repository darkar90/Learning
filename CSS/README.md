# TABLA DE INICIO  

[Pseudoclase y Pseudoelemento](#pseudo-clases-y-pseudo-elementos)  
[Anatomia de un reglas CSS](#anatomia-de-una-regla-de-css)  
[Modelo de caja](#modelo-de-la-caja)  
[Hrenecia](#herencia)  
[Especifidad con selectores](#especificidad-en-selectores)  
[Combinadores](#combinadores)  
[Medidas](#medidas)  

**CSS** significa **Cascading Stule Sheet** es la herramineta con el cual le damos estilo a las paginas  

## Como utilizamos css?: por etiquetas, selectores, clases y ID 
----  
``` html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Clase CSS</title>
  <link rel="stylesheet" href="./style.css" />
</head>
<body>
  <main>
    <p class="parrafo">Soy un texto</p>
    <p id="texto">Soy otro texto</p>
  </main>
</body>
</html>

```  
CSS 
``` css
p {
  color: blue;
  font-size: 40px;
}

/* class */
.parrafo {
  color: red;
}

/* ID */
#texto {
  color: yellow;
  font-size: 24px;
}
```  
## Pseudo clases y Pseudo elementos   
----  
Las pseudoclases junto a los pseudoelementos permiten aplicar un estilo a un elemento  

**Pseudoelemento**  
``` css
.main-nav__item a:hover{
  color:blue;
}
```
[pseudoelemento](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-elements)

**Pseudoclases**  
``` css
.main-nav__item a::after{
  content:" | ";
}
```  
[pseudoclases](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes)  


## Anatomia de una regla de CSS  
----
``` css
/*selector = p*/
p {
  color: red;  /*declaracion*/
}

/* propiedad = color 
   valor de la propiedad = red */
```   
## Modelo de la caja 
----  
[box-sizing o tamaño de la caja](https://developer.mozilla.org/es/docs/Web/CSS/box-sizing)  

## Herencia   
----  
**inherit** es el valor medio de una keyword que especifica que a la propiedad que se le apliquemos debe heredar los valores de su padre en otras palabras significa **"usar el valor de mi padre"** 

``` css 
html {
  font-size:75%;
  font-family:Verdana,Geneva,Tahoma,sans-serif
  }
h1 {
    font-size:inherit
   }
```  
## Especificidad en selectores  
----  

| SELECTORES   | ESPECIFICIDAD  |
|--------------|----------------|  
| !important   |  1,0,0,0,0     |
| Inline Style |  0,1,0,0,0     |
|   #ID        |  0,0,1,0,0     |
|  .class      |  0,0,0,1,0     |
|    tag       |  0,0,0,0,1     |   

``` html
<body>
<header class="page-header">
  <h1 id="page-title" class="title">Empresa</h1>
    <nav>
      <ul id="main-nav" class="nav">
        <li><a href="">Home</a></li>
        <li><a href="">Cursos</a></li>
        <li><a href="">Instructores</a></li>
        <li>
           <a href="" class="blog">Blog</a>
        </li>
      </ul>
    </nav>
</header>
</body>
```  
``` css
* {
  box-sizing:border-box;
  margin:0;padding:0
  } 
h1 {
    color:purple;
    font-family:serif;
    margin-bottom:10px
    }
.title {
    font-size:18px;
    font-family:monospace
    }
.nav {
  margin-top:10px;
  list-style-type:none;
  padding-left:0
  }
.nav li {
  display:inline-block
  }
.nav a {
  color:#fff;
  background-color:#13a4a4;
  padding:5px;
  border-radius:2px;
  text-decoration:none
  }
.nav .blog {
  background-color:red
  } 
```  
## Combinadores  
----  
Nos permite combinar múltiples selectores y crear una mayor especificidad  

| Hermanos adyacentes cercanos |  Hermano general | 
|------------------------------|------------------| 
|     div + p {....}           |  div ~ p {....}  |   


|       Hijo                |    Descendiente      |  
|---------------------------|----------------------|  
|       div > p { ...}      |    div p {....}      |  


- **Hermano adyacente o cercano**: se le aplica a toda las etiquetas que esten cerca del de la primera etiqueta  

``` html div>
  <h2>uno</h2>     <!--hermano adyacente-->
  <p>dos</p>
  <h2>tres</h2>    
  <h3>cuatro</h3>
  <p>cinco</p>
</div>

```  
``` css 
h2 + p {
  color: red;
}
```

- **Hermano general**: se modifica todas la etiquetas que tengan como hermano genral una etiqueta  
``` html 
<div>
  <h2>uno</h2>     <!--hermano genral-->
  <p>dos</p>
  <h2>tres</h2>    <!--hermano general-->
  <h3>cuatro</h3>
  <p>cinco</p>
</div>
```
``` css
h2 ~ p {
  color: red;
}
```  

- **Hijo**: una etiqueta tiene que ser hija directa de otra etiqueta para poder agregar cambios 

``` html 
<div>
  <article>
    <p>soy un texto</p>
  </article>
    <article>
    <p>soy un texto</p>
  </article>
  <section>
    <div>
      <p>soy un texto</p>
    </div>
  </section>
  <p>soy un texto</p>
</div>
```  
``` css 
div > p {
  color: red; 
} 
```  
- **Desendiente**: todas las etiquetas que esten dentro de un contenedor o una etiqueta  

``` html 
<div>
  <article>
    <p>soy un texto</p>
  </article>
    <article>
    <p>soy un texto</p>
  </article>
  <section>
    <div>
      <p>soy un texto</p>
    </div>
  </section>
  <p>soy un texto</p>
</div>
```  
``` css 
div  p {
  color: red; 
}  
```  
[Conbinadores](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Combinators)  

## Medidas  
----  
Tenemos 2 parametros  **medidas Relativas** y **Medidas absolutas**  
- **Medidas absolutas**: No va a cambiar sin inportar el tamaño de la pantalla  

- **Medidas relativas**: Si van a cambiar el tamaño con relacion al dispositivo donde se vea 

|   Absolutas     |   Relativas             |
|-----------------|-------------------------|
|      px         |        %                |
|                 |       em                |
|                 |     rem(root em)        |
|                 |  max-width / max-height |
|                 |  min-width / min-height | 
|                 |  vw ( viewport width )  | 
|                 |  vh ( viewport height)  |        

**Medidas EM** : Lo que hace **em** es que toma el tamaño de fuente que tenga el padre directo 
``` css 
.container {
   font-size: 20px
   }

.container div {
    font-size: 2em
   }
```  
**Medidas REM** : Rem siempre va a tener referencia a el tamaño de fuente que tenga la etiqueta html 

``` css
html {
  font-size: 62.5%;
}
p {
  font-size: 1.6rem;
}

``` 
- Lo que siempre debe ir en todos los archivos de CSS es : 

``` css 
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
html {
  font-size: 62.5%;
}

```  

## Max/Min width  
----  
Pone maximos y minimos a lo ancho seria una forma de hacer ciertos contenedores flexibles de la misma manera se puede usar con **height**

html
``` html 
</head>
<body>
  <main>
    <section></section>
  </main>
</body>
</html>
```  
Css
``` css 
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

main {
  width: 100vw;
  height: 100vh;
  background-color: purple;
}

section {
  width: 100%;
  min-width: 320px;
  max-width: 500px;
  height: 850px;
  background-color: red;
  margin: 0 auto;
} 
```   
## Position 
----  
 |     Position    |                  | 
 |-----------------|------------------|
 |  static         | por defecto      |
 | absolute        |                  |
 | relative        |                  |
 |   fixed         |                  | 
 |   sticky        |                  |

 - **static** : Cuando estamos en static no podemos usar el botton el left o el rigth  

 [Position](https://css-tricks.com/almanac/properties/p/position/)  
