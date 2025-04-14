
# Documentación del Software: Calculadora en Python con POO

## Descripción General de la Práctica

Este proyecto tiene como finalidad aplicar los principios de la **Programación Orientada a Objetos (POO)** mediante la implementación de dos clases principales: `Calculadora` y `CalculadoraFactorial`.  
La práctica permite realizar operaciones básicas como suma, resta, multiplicación y división, así como el cálculo del factorial de un número, aprovechando el concepto de **herencia**, entre otros pilares fundamentales de la POO.

---

## Configuración del Entorno y Ejecución del Archivo Principal

### Requisitos

- Python 3.x instalado

### Archivos involucrados

- `main.py`: archivo principal de ejecución
- `calculadora_poo.py`: contiene la clase `Calculadora`
- `factorial_poo.py`: contiene la clase `CalculadoraFactorial`

### Estructura del proyecto

```bash
calculadora/
│
├── main.py
├── calculadora_poo.py
└── factorial_poo.py
```

### Cómo ejecutar

Desde la terminal, ubicándote en el directorio del proyecto, ejecutá:

```bash
python main.py
```

---

## Descripción y Forma de Uso de la Clase `Calculadora`

La clase `Calculadora` representa una calculadora estándar que puede realizar operaciones básicas: **suma, resta, multiplicación y división**.

### Métodos públicos

- `sumar(a, b)`: retorna la suma de `a` y `b`.
- `restar(a, b)`: retorna la diferencia entre `a` y `b`.
- `multiplicar(a, b)`: retorna el producto de `a` y `b`.
- `dividir(a, b)`: retorna el cociente de `a` entre `b`, con manejo de división por cero.

### Forma de uso

```python
from calculadora_poo import Calculadora

calc = Calculadora()
print(calc.sumar(2, 5))       # Suma: 2 y 5 = 7
print(calc.restar(10, 9))     # Resta: 10 y 9 = 1
print(calc.multiplicar(5, 9)) # Multiplicar: 5 y 9 = 45
print(calc.dividir(150, 6))   # Dividir: 150 y 6 = 25.0
```

---

## Principios de la POO aplicados en la clase `Calculadora`

| Principio       | Cómo se aplica                                                                 |
|-----------------|----------------------------------------------------------------------------------|
| Abstracción     | Representa el concepto de calculadora simple con sus operaciones básicas.       |
| Encapsulamiento | Usa atributos privados (`__resultado`) y métodos protegidos (`_multiplicar`).   |
| Modularidad     | Cada operación es un método separado, claro y reutilizable.                     |
| Reutilización   | Puede ser usada como clase base para otras calculadoras más complejas.          |

---

## Descripción y Forma de Uso de la Clase `CalculadoraFactorial`

La clase `CalculadoraFactorial` **hereda** de la clase `Calculadora` y agrega una funcionalidad adicional: **el cálculo del factorial de un número**.

### Métodos públicos

- `calcular()`: calcula el factorial del número recibido en el constructor.

### Forma de uso

```python
from factorial_poo import CalculadoraFactorial

calc_fact = CalculadoraFactorial(numero=5)
print(calc_fact.calcular())   # Factorial: 5 = 120
```

---

## Principios de la POO aplicados en la clase `CalculadoraFactorial`

| Principio       | Cómo se aplica                                                                 |
|-----------------|----------------------------------------------------------------------------------|
| Herencia        | Extiende la clase `Calculadora`, reutilizando su estructura y métodos.          |
| Encapsulamiento | Usa atributos propios (`numero`) y accede a métodos protegidos de la clase base.|
| Abstracción     | Representa una calculadora especializada en cálculos factoriales.               |
| Reutilización   | Reutiliza `_multiplicar()` y `_mostrar_operacion()` de la clase `Calculadora`.  |

---

## Diferencia entre la implementación procedimental y orientada a objetos

| Aspecto                         | Enfoque Procedimental                               | Enfoque Orientado a Objetos                               |
|---------------------------------|------------------------------------------------------|------------------------------------------------------------|
| Estructura                      | Basado en funciones sueltas                         | Basado en clases y objetos                                 |
| Organización del código         | Menos modular, más difícil de mantener              | Modular, más fácil de escalar y mantener                   |
| Reutilización                   | Difícil de reutilizar sin copiar código             | Reutilización mediante herencia y composición              |
| Legibilidad y cohesión          | Funciones sin contexto explícito                    | Métodos agrupados en clases con un propósito claro         |
| Encapsulamiento                 | Variables y lógica expuestas                        | Atributos protegidos o privados                            |
| Extensión de funcionalidades    | Requiere modificar funciones originales             | Se pueden crear nuevas clases que extienden las existentes |

---
