# CURSO BASICO DE PYTHON

## TABLA DE CONTENIDO

- [CONCEPTOS BASICOS](#conceptos-basicos)
  - [Operadore aritmericos](#operadore-aritmeticos)
  - [Variables](#variables)
  - [Tipo de Datos](#tipos-de-datos)

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
