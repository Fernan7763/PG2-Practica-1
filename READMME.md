# Practica 1

En esta práctica se implementa una calculadora en Python que permite realizar
operaciones aritméticas básicas como suma, resta, multiplicación y división.

Del mismo modo, se implementa una calculadora de factorial que aplica principios
de herencia y polimorfismo.

## Preparación del entorno

## Implementacion Calculadora Estandar

Este módulo implementa una calculadora estándar que permite realizar operaciones
aritméticas básicas como suma, resta, multiplicación y división. El modo de
funcionamiento es el siguiente:

```python
from calculadora_poo import Calculadora

calculadora_1 = Calculadora()

print(calculadora_1.sumar(2, 5))
print(calculadora_1.restar(10, 9))
print(calculadora_1.multiplicar(5, 9))
print(calculadora_1.dividir(150, 6))
```

## Implementacion Calculadora Factorial

Este módulo implementa una calculadora factorial que hereda de la clase
Calculadora. Permite calcular el factorial de un número entero positivo. El modo
de funcionamiento es el siguiente:

```python
from calculadora_poo import CalculadoraFactorial
calculadora_factorial = CalculadoraFactorial(numero=5)
print(calculadora_factorial.calcular())
```