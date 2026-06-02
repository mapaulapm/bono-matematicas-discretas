# Bono de Programación - Matemáticas Discretas I (UNAL)

## Descripción general

Este proyecto implementa soluciones a problemas de conteo del bono de programación del curso Matemáticas Discretas I.



---

# Problemas implementados

## Problema 2: Calculadora de combinaciones

### Descripción

Se implementa una calculadora general de combinaciones, que permite calcular el número de formas de escoger r elementos de un conjunto de n elementos sin importar el orden.

---

### Fórmula matemática

\[
\binom{n}{r} = \frac{n!}{r!(n-r)!}
\]

---

### Funcionalidades

- Cálculo de \( \binom{n}{r} \)
- Validación de entradas (0 ≤ r ≤ n)
- Cálculo de factorial
- Generación de fila del triángulo de Pascal
- Verificación de simetría:
  \[
  \binom{n}{r} = \binom{n}{n-r}
  \]

---

## Problema 6: Permutaciones circulares con restricciones

## Descripción del problema

Construya un programa que cuente arreglos circulares de \(n\) objetos distintos.

En una disposición circular, dos arreglos que solo difieren por rotación se consideran iguales, por lo que se elimina la simetría rotacional.

---

## Base matemática

El número de permutaciones circulares de \(n\) elementos es:

$$
(n-1)!
$$

Esto se debe a que se fija un elemento como referencia para eliminar las rotaciones equivalentes, y se permutan los \(n-1\) restantes.

---

## Restricciones implementadas

### 1. Dos personas deben quedar juntas

Se agrupan como un solo bloque:

$$
2 \cdot (n-2)!
$$


### 2. Dos personas no pueden quedar juntas

Se usa el principio de complemento:

$$
(n-1)! - 2 \cdot (n-2)!
$$



### 3. Un líder debe quedar entre dos personas específicas

El líder se fija como referencia y las dos personas pueden ubicarse en ambos lados:

$$
2 \cdot (n-3)!
$$



### 4. Varios grupos deben sentarse separados

Se modela mediante agrupación en bloques y uso del principio de exclusión (dependiendo del tamaño de los grupos).

---

## Justificación de la simetría circular

En una mesa circular, cualquier rotación de los elementos no genera una disposición nueva. Por ejemplo, todas las rotaciones de una misma configuración representan la misma organización.

Por esta razón, se fija una persona como referencia, reduciendo el problema a permutar los \(n-1\) elementos restantes.


# Cómo ejecutar el programa

## Requisitos
- Python 3.x

## Ejecución

```bash
python main.py
