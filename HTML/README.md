# TABLA DE CONTENIDO

[HTML](#html)

- [Anatomia de una pagina Web](#anatomia-de-una-pagina-web)
- [head](#head)
- [body](#body)
- [Anatomia de una etiqueta HTML](#anatomia-de-una-etiqueta-html)  

[Etiquetas Multimedia]()

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
 

