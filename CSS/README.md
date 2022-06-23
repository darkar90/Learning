# TABLA DE INICIO  

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

