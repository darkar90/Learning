# CURSO BASICO DE PYTHON

## TABLA DE CONTENIDO

- [CONCEPTOS BASICOS](#conceptos-basicos)
  - [Operadore aritmericos](#operadore-aritmeticos)
  - [Variables](#variables)
  - [Tipo de Datos](#tipos-de-datos)
- [HERRAMIENTAS PARA PROGRAMAR](#condicionales)
  - [Aprendiendo a no repetir codigo](#aprendiendo-a-no-repetir-código)
  - [Trabajando con textos](#trabajando-con-textos)
- [BUCLES](#bucles)
- [ESTRUCTURA DE DATOS](#estructura-de-datos)

## **CONCEPTOS BASICOS**

---

## Operadore Aritmeticos

**Suma** = 5 + 5  
**Resta** = 5 - 5  
**Multiplicacion** = 5 _ 5  
**División** (con decimales) = 21 / 5  
**División** (sin decimales) = 21 // 5  
**Resto de la división** = 21 % 5  
**Potecia** = 2 _ 2

**Raiz cuadrada**

```python
math.sqrt(9)
 3.0
math.sqrt(11.11)
 3.3331666624997918
math.sqrt(Decimal('6.25'))
 2.5
```

Python respeta la separacion de terminos , para recordar el orden de las operaciones en algebra usamos **PEMDAS**

- Parentesis
- Exponentes o raices
- Multiplicaciones
- Divisiones
- Suma y restas

## Variables

- Que es una variable ?
  - una variable es un lugar de memoria en donde podemos guardar objetos
  ```python
  var1 = 5
  var2 = 10
  ```
- Tipos de Variables
_ a = 28 → int (entero)  
 _ b = 1.5 → float (decimales)  
 _ c = “Hello” → str (string o cadena de texto)  
 _ d = True → boolean (verdadero o falso)  
 _ e = None → NoneType (Sin valor)  
 _ f = “5” → str (5 y “5” no son lo mismo. La primera es un entero y la segunda una cadena de texto)
<div align="right">
  <small><a href="#tabla-de-contenido">🡡 volver al inicio</a></small>
</div>

## Tipos de Datos

- Tipos de datos Primitivos
  - **Integers**: números Enteros
  - **Floats**: números de punto flotante (decimales)
  - **Strings**: cadena de caracteres (texto)
  - **Boolean**: boolenaos (Verdadero o Falso)
- Tipos de datos Adicionales
  - **Datos en texto**: str
  - **Datos numéricos**: int, float, complex
  - **Datos en secuencia**: list, tuple, range
  - **Datos de mapeo**: dict
  - **Set Types**: set, frozenset
  - **Datos booleanos**: bool
  - **Datos binarios**: bytes, bytearray, memoryview

¿Coomo convertir un datoa un tipo diferente?

```python
    int(var)   variable a entero
    float(var) variable a flotante
    str(var)   variable a texto
    bool(var)  variable a booleano
    abs(var)   variable a valor absoluto
```

Ejemplo

```python
>>> number1 = input("Escribe un número: ")
Escribe un número: 4
>>> number2 = input("Escribe otro número: ")
Escribe un número: 5
>>> numero1 + numero 2
=> '45' <== Se concatenan
```

Solucion

```python
>>> number1 = int(input("Escribe un numero: "))
Escribe un numero: 100
>>> number2 = int(input("Escribe otro numero: "))
Escribe otro numero: 300
>>> number1 + number2
=> 400
```

<div align="right">
  <small><a href="#tabla-de-contenido">🡡 volver al inicio</a></small>
</div>

## Operadores Logicos y de Comparacion

- **Operador Logico**

  - **and** ( y ): compara dos valores, y si ambos son verdaderos, devuelve True.
  - **or** ( ó ): si al comparar dos valores y uno de los dos se cumple, devuelve True. Solo devuelve falso cuando los dos valores no se cumplen.
  - **not** ( no): invierte el valor de una variable, dando el valor contrario al de la variable evaluada.

- **Operador de Compraracion**
  - **== ( igual qué )**: determina si dos valores son iguales o no.
  - **!= (diferente de)**: determina si dos valores son distintos o no. Si los valores son diferentes devuelve True, si son iguales devuelve False.
  - **> (mayor que)**: compara dos valores, y determina si es mayor que el otro.
  - **< (menor que)**: compara dos valores y determina si es menor que el otro.
  - **>= (mayor o igual)**: compara dos valores y determinas si es mayor o igual que el otro.
  - **<= (menor o igual)**: compara dos valores y determinas si es menor o igual que el otro.

## **HERRAMIENTAS PARA PROGRAMAR**

---

## Condicionales

Las condicionales son decisiones que se establecen deacuerdo a los parárametros que indiquemos para obtener un tipo de resultado deseado

**IF (si)**  
se usa para condición principal

**ELIF (si no )**  
en caso de la condición principal no se cumpla se pude utilizar para agregar otra condición

**ELSE (sino)**  
en caso de que la(s) condición(es) anterior(es) no se cumplan, se ejecuta como alternativa sin condicional

**Ejemplo**

```python

#convierte pesos mexicanos, argentinos y colombianos a dólares

# """ """ permite crear strings multilineas
menu = """
Bienvenido al conversor de monedas multipais

1-Pesos Mexicanos
2-Pesos Colombianos
3-Pesos Argentinos

Elige una opción:

"""
# de derecha a izquierda: llamo a la funcion input, le paso la variable menu para que la imprima y reciba el número que el usuario escogió, lo convierto a int y lo guardo en la variable 'opcion'
opcion = int(input(menu))

if opcion == 1: #pesos mexicanos
	#pregunto al usuario la cantidad a convertir
	pesos = input('¿Cuántos pesos mexicanos tienes?: ')
	#convierto a float para mejor manejo de datos
	pesos = float(pesos)
	#escribo el valor del dolar en pesos mexicanos
	tipo_de_cambio = 21.5
elif opcion == 2: #pesos colombianos
	#pregunto al usuario la cantidad a convertir
	pesos = input('¿Cuántos pesos colombianos tienes?: ')
	#convierto a float para mejor manejo de datos
	pesos = float(pesos)
	#escribo el valor del dolar en pesos colombianos
	tipo_de_cambio = 3715.01
elif opcion == 3: #pesos argentinos
	#pregunto al usuario la cantidad a convertir
	pesos = input('¿Cuántos pesos argentinos tienes?: ')
	#convierto a float para mejor manejo de datos
	pesos = float(pesos)
	#escribo el valor del dolar en pesos argentinos
	tipo_de_cambio = 74.44
else:  #el usuario escribió algo diferente
	print('Escribe una opción correcta: ')


#hago la conversión
dolares = pesos / tipo_de_cambio
#redondeo los dólares a dos decimales
dolares = round(dolares, 2)
#convierto el float de dolares a un string
dolares = str(dolares)

#imprimo el valor de la conversion. Se pueden sumar (concatenar) strings con '+'
print('Tienes $' + dolares +' dólares')
```

<div align="right">
  <small><a href="#tabla-de-contenido">🡡 volver al inicio</a></small>
</div>

## APRENDIENDO A NO REPETIR CÓDIGO

---

- Para ya no estar repitieno código usamaos las **FUNCIONES**

**FUNCIONES**  
 Las funciones ayudan a optimizar el código. Es decir, utilizar la menor cantidad de líneas dentro del código y evitar escribir acciones repetitivas.

Esto nos sirve para entregar un código más limpio y con buenas prácticas, que no desperdicia recursos innecesariamente. En Python, para definir funciones empleamos `def`

Gracias a def, podemos “definir” funciones que emplearemos más tarde. Una función, en programación, es un grupo de instrucciones con un objetivo en particular y que se ejecuta cuando es “invocada”.

**Ejemplo**

```python
def conversacion(opcion):
  print('Hola')
  print('Cómo estás')
  print('Elegiste la opcion: ' + str(opcion))
  print('Adiós')

opcion = int(input('Ingrese una opción (1, 2, 3): '))

if opcion == 1:
  conversacion(opcion)

elif opcion == 2:
  conversacion(opcion)

elif opcion == 3:
  conversacion(opcion)

else:
  print('Escribe una opción correcta.')
```

- **ENTRIPOINT**  
  Punto de entrada

```python
    if __name__ == '__main__':
    run()
```

Una vez que python se encuentra con el entritpoint empieza a correr todo lo que esta debajo

<div align="right">
  <small><a href="#tabla-de-contenido">🡡 volver al inicio</a></small>
</div>

## TRABAJANDO CON TEXTOS

---

- **Cadena de Caracteres**

  Para trabajar con cadenas de texto en Python, vamos a aplicar una serie de métodos a las variables que hayamos creado anteriormente.

  **Método:** es una función especial, que existe para un tipo de dato en particular. Por ejemplo, si queremos que el texto ingresado se transforme en mayúsculas.

  **Métodos para trabajar con texto en Python**

  - **variable.strip():** El método strip eliminará todos los caracteres vacíos que pueda contener la variable

  - **variable.lower():** El método lower convertirá a las letras en minúsculas.

  - **variable.upper():** El método upper convertirá a las letras en mayúsculas.

  - **variable.capitalize():** El método capitalize convertirá a la primera letra de la cadena de caracteres en mayúscula.

  - **variable.replace (‘o’, ‘a’):** El método replace remplazará un caracterer por otro. En este caso remplazará todas las ‘o’ por el caracter ‘a’.

  - **len(variable):** Te indica la longitud de la cadena de texto dentro de la variable en ese momento.

- **SLICES**  
   En Python, los slices, traducidos al español como “rebanadas”, nos permiten dividir los caracteres de un string de múltiples formas. A continuación, realizaremos un ejemplo cómo utilizarlos:

  **Ejemplo**

  ```python
  nombre = "Francisco"
  nombre
  "Francisco"
  nombre[0 : 3)
  ```

  Arranca desde el primer índice hasta llegar antes del 3° índice.  
   El resultado sería  
   "Fra"

  ```python
      nombre[1:7:2]
  ```

  Arranca desde el índice 1 hasta llegar antes del 7, pero pasos de 2 en 2, ya que eso es lo que nos indica el 3er parámetro, el cual es 2.  
   El resultado sería
  "rni"

  ```python
  nombre[1::3]
  ```

  Arranca desde el índice 1 hasta el final del string (al no haber ningún 2° parámetro, significa que va hasta el final), pero en pasos de 3 en 3.  
   El resultado sería
  "rcc"

  ```python
  nombre[::-1]
  ```

  Al no haber parámetro en las 2 primeras posiciones, se interpreta que se arranca desde el inicio hasta el final, pero en pasos de 1 en 1 con la palabra al revés, porque es -1.  
   El resultado sería
  "ocsicnarF"

<div align="right">
  <small><a href="#tabla-de-contenido">🡡 volver al inicio</a></small>
</div>

## BUCLES

---

**Un bucle es un ciclo continuo en todos los lenguajes de programación que nos permite iterar sobre nuestros pasos:** imagina un contador cíclico (1,2,3,4,5,6…) donde puedes agregar un paso más sobre tu programa principal.

```python
def run():
    LIMITE = 1000000

    contador = 0
    potencia_2 = 2**contador
    while potencia_2 < LIMITE:
        print('2 elevado a ' + str(contador) +  ' es igual a: ' + str(potencia_2))
        contador = contador + 1
        potencia_2 = 2**contador


if __name__ == '__main__':
    run()

```

- **Ciclo WHILE**  
  Un bucle while permite repetir la ejecución de un grupo de instrucciones mientras se cumpla una condición (es decir, mientras la condición tenga el valor True).  
  **Ejemplo**

```python
while condicion:
    cuerpo del bucle
```

- **Ciclo FOR**  
  El bucle **for** es una forma de hacer mas simplificado el código

  Tabla del 11

```python
for i in range(10):
    print(11 * i)
```

Para la variable **i** en el rango que va de **0** a **9** se imprime en cada vuelta del **ciclo** por **11** por el valor de la variable **i**

- **Recorriendo un string con FOR**  
  Recorrer un string con el ciclo For es tomar la cadena de caracteres y separarlas una a una. De este modo, quedaría el comando:

```python
def run():
    frase = input("Escribe una frase: ")
    for caracter in frase:
        print(caracter.upper())

if __name__ == "__main__":
    run()
```

Donde usaremos la variable frase para recorrer la frase que se escriba en el input. Cuando se escriba una frase, se recorrerá cambiando todas las letras a mayúsculas.

- **Interumpiendo ciclos con BREAK y CONTINUE**

  - **CONTINUE**  
    La instrucción continue en Python devuelve el control al comienzo del ciclo while o ciclo for. Esta instrucción rechaza todas las declaraciones restantes en la iteración actual del ciclo y mueve el control de regreso a la parte superior del mismo.

  ```python
  def run():
    for contador in range(1000):
        if contador % 2 != 0:
            continue
        print(contador)

   if __name__ == '__main__':
    run()
  ```

  - **BREAK**  
    La instrucción break en Python termina el ciclo actual y reanuda la ejecución en la siguiente instrucción. En otras palabras, break rompe el ciclo entero mientras que continue solo rompe la vuelta actual.

  ```python
  def run():
    for i in range(10000):
        print(i)
        if i == 5678:
            break

   if __name__ == '__main__':
   run()
  ```

<div align="right">
  <small><a href="#tabla-de-contenido">🡡 volver al inicio</a></small>
</div>

## Estructura de Datos

---

- **Listas**

  Las listas nos permiten guardar múltiples valores en una sola variable. Estas listas en Python nos permiten guardar elementos del mismo tipo o diferentes, por lo que podemos tener strings, números enteros y decimales juntos en una misma variable. Las listas también son conocidas como arrays en otros lenguajes programación.

  - **Declarar Listas**
    ```python
      my_lista = []
      my_lista = list()
    ```
  - **Unir Listas**
    ```python
     my_lista = [1]
     my_lista2 = [2,3,4]
     my_lista3 = my_lista + my_lista2
     my_lista3 # [1,2,3,4]
    ```
  - **Partir listas con Slices**
    ```python
     my_lista = [1,2,3]
     my_lista[1:] = [2,3]
    ```
  - **Extender una Lista**
    ```python
     my_lista = [1]
     my_lista2 = [2,3,4]
     my_lista.extend(my_lista2) # [1,2,3,4]
    ```
  - **Multiplicar una Lista**
    ```python
     my_lista = ['a']
     my_lista2 = my_lista * 5
     my_lista2 # ['a','a','a','a','a']
    ```
  - **Eliminar el ultimo elemento de una Lista**

    ```python
     my_lista = [1,2,3,4,5]
     my_lista = my_lista.pop()
     my_lista # [1,2,3,4]

    ```

  - **Ordenar una Lista**
    ```python
     my_lista = [2,1,5,4,3]
     my_lista = my_lista.sort()
     my_lista # [1,2,3,4,5]
    ```
  - **Eliminar un elemento**
    ```python
     my_lista = [1,2,3,4,5]
     del my_lista[0]
     my_lista # [2,3,4,5]
    ```
  - **Eliminar si conocemos el Valor**
    ```python
     my_lista = [1,2,3,4,5]
     my_lista.remove(3)
     my_lista #[1,2,4,5]
    ```
  - **Añadir un elemento al final**
    ```python
     my_lista = [1,2,3,4,5]
     my_lista.append(6)
     my_lista # [1,2,3,4,5,6]
    ```
  - **Organizar una Lista**  
     `python my_lista = [2,5,1,3,4] my_lista.sort() #[1,2,3,4,5] `  
    **Métodos adicionales para listas**

  - **.sorted()**
    También ordena como sort() pero modifica la lista inicial
  - **.clear()**
    Vacía la lista
  - **.count()**
    Cuenta las veces que esta un elemento en lista
  - **.index()**
    Indica la posición donde esta un elemento de la lista
  - **.insert()**
    Inserta un elemento en una posición dada ej: lista.insert(posición,item)
  - **.reverse()**
    Le da la vuelta a una lista

- **Tuplas**  
  Las tuplas son estructuras de datos inmutables. Es decir, no puedes modificar una tupla a agregando o quitando un valor. Lo único que puedes hacer es definir de nuevo esa tupla a. Los objetos inmutables (como los strings) son tipos de datos para Python que apuntan a un lugar específico en memoria y que su contenido no puede ser cambiado. Al cambiar el contenido predefiniendo el contenido de la variable a, entonces cambiará su posición en memoria.
