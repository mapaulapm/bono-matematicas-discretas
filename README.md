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

### Descripción

Se estudian las formas de organizar n personas en una mesa circular, donde las rotaciones no generan arreglos distintos.

Además, se incluyen restricciones como:
- Dos personas que deben estar juntas
- Dos personas que no pueden estar juntas
- Grupos que deben permanecer separados
- Un líder que debe quedar entre dos personas específicas

---

### Base matemática

\[
(n - 1)!
\]

---


# Cómo ejecutar el programa

## Requisitos
- Python 3.x

## Ejecución

```bash
python main.py
