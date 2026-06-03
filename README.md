# Bono de Programación - Matemáticas Discretas I (UNAL)

## Descripción general

Este proyecto implementa soluciones a problemas de conteo del bono de programación del curso Matemáticas Discretas I.



---

# Problemas implementados
# Problema 3: Conteo de cadenas binarias con restricciones

## Descripción del problema

Construya un programa que cuente cadenas binarias de longitud (n) bajo distintas restricciones relacionadas con la cantidad de unos presentes en la cadena.

Una cadena binaria es una secuencia formada únicamente por los símbolos (0) y (1).

El programa permite calcular la cantidad de cadenas que cumplen diferentes condiciones y, opcionalmente, listar todas las cadenas cuando el tamaño es pequeño.

---

## Base matemática

### 1. Número total de cadenas binarias de longitud (n)

Cada posición puede tomar dos valores posibles ((0) o (1)), por lo que el número total de cadenas es:

$$
2^n
$$

---

### 2. Cadenas con exactamente (k) unos

Se deben escoger las (k) posiciones donde aparecerán los unos entre las (n) posiciones disponibles:

$$
\binom{n}{k}
$$

---

### 3. Cadenas con a lo sumo (k) unos

Se suman todos los casos posibles desde (0) hasta (k) unos:

$$
\sum_{i=0}^{k} \binom{n}{i}
$$

---

### 4. Cadenas con al menos (k) unos

Se suman todos los casos posibles desde (k) hasta (n) unos:

$$
\sum_{i=k}^{n} \binom{n}{i}
$$

---

### 5. Cadenas con igual número de ceros y unos

Esta condición solo es posible cuando (n) es par.

Se seleccionan las posiciones de los unos:

$$
\binom{n}{n/2}
$$

---

## Restricciones implementadas

### 1. Todas las cadenas binarias de longitud (n)

Calcula:

$$
2^n
$$

---

### 2. Exactamente (k) unos

Calcula:

$$
\binom{n}{k}
$$



### 3. A lo sumo (k) unos

Calcula:

$$
\sum_{i=0}^{k} \binom{n}{i}
$$



### 4. Al menos (k) unos

Calcula:

$$
\sum_{i=k}^{n} \binom{n}{i}
$$



### 5. Igual número de ceros y unos

Si (n) es par:

$$
\binom{n}{n/2}
$$

Si (n) es impar, el programa informa que no existe ninguna cadena que cumpla la condición.



## Extensión opcional

Cuando:

$$
n \leq 10
$$

el programa genera y muestra explícitamente todas las cadenas binarias que satisfacen la restricción seleccionada.

Esto permite verificar visualmente los resultados obtenidos mediante las fórmulas combinatorias.

---

## Justificación combinatoria

Las restricciones implementadas se fundamentan en el principio de conteo y en los coeficientes binomiales.

Cada cadena binaria puede interpretarse como una selección de posiciones donde aparecen unos. Por esta razón, el número de cadenas que contienen exactamente (k) unos coincide con el número de formas de escoger (k) posiciones entre (n), es decir:

$$
\binom{n}{k}
$$

Las demás restricciones se obtienen sumando los casos correspondientes o aplicando directamente propiedades de los coeficientes binomiales.

---

## Complejidad

### Conteo

Las operaciones de conteo mediante combinaciones tienen complejidad:

$$
O(n)
$$

o menor dependiendo de la implementación de los coeficientes binomiales.

### Generación de cadenas

La generación explícita de todas las cadenas binarias requiere:

$$
O(2^n)
$$

por lo que se limita a valores pequeños de (n).

---

## Ejemplo

Para:

$$
n = 5,\quad k = 2
$$

el número de cadenas binarias con exactamente dos unos es:

$$
\binom{5}{2}=10
$$

Las cadenas correspondientes son:

```text
00011
00101
00110
01001
01010
01100
10001
10010
10100
11000
```


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
