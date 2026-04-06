# DIVISIBILIDAD I - Semana 5

## 1. Introducción a la Divisibilidad

La divisibilidad es la parte de la aritmética que estudia las condiciones que debe cumplir un número entero para poder dividir exactamente a otro número entero. Decimos que un número entero \(a\) es **divisible** por otro entero \(b \neq 0\) si existe un entero \(k\) tal que:

\[
a = b \cdot k
\]

Notación: \(b \mid a\) (se lee "\(b\) divide a \(a\)" o "\(a\) es múltiplo de \(b\)").

Si no existe tal \(k\), escribimos \(b \nmid a\).

### Ejemplos básicos:
- \(3 \mid 12\) porque \(12 = 3 \cdot 4\).
- \(5 \mid 35\) porque \(35 = 5 \cdot 7\).
- \(4 \nmid 14\) porque no existe entero \(k\) con \(14 = 4k\).

---

## 2. Multiplicidad

El concepto de **multiplicidad** se refiere a la expresión de un número como múltiplo de otro. Decimos que un número \(N\) es **múltiplo** de \(d\) si \(N = d \cdot k\), con \(k \in \mathbb{Z}\).

### Notación de múltiplos:
- El conjunto de todos los múltiplos de \(d\) se escribe:  
  \[
  \dot{d} = \{ \dots, -2d, -d, 0, d, 2d, 3d, \dots \}
  \]
- En muchos problemas usamos la notación \(N = \dot{d}\) para indicar que \(N\) es múltiplo de \(d\).

### Propiedades inmediatas:
1. \(1 \mid N\) para todo \(N\) entero.
2. \(N \mid N\) (propiedad reflexiva).
3. Si \(a \mid b\) y \(b \mid c\) entonces \(a \mid c\) (transitividad).
4. El cero es múltiplo de cualquier número: \(d \mid 0\) porque \(0 = d \cdot 0\).

### Ejemplo:
Escribe todos los múltiplos de 7 entre -20 y 20.  
Solución: \(-14, -7, 0, 7, 14\).

---

## 3. Principios Fundamentales de la Divisibilidad

Estos principios son teoremas básicos que permiten operar con divisibilidad.

### Teorema 1: Combinación lineal
Si \(d \mid a\) y \(d \mid b\), entonces para cualesquiera enteros \(m, n\) se cumple:
\[
d \mid (m a + n b)
\]
Es decir, \(d\) divide cualquier combinación lineal entera de \(a\) y \(b\).

**Demostración breve**:  
\(a = d \cdot q_1\), \(b = d \cdot q_2\) ⇒ \(m a + n b = d (m q_1 + n q_2)\).

### Teorema 2: Divisibilidad del producto
Si \(d \mid a\), entonces \(d \mid a \cdot c\) para cualquier entero \(c\).

### Teorema 3: Ley de cancelación
Si \(c \neq 0\) y \(c \cdot a \mid c \cdot b\) entonces \(a \mid b\).

### Teorema 4: Comparación con el divisor
Si \(a \mid b\) y \(b \neq 0\), entonces \(|a| \le |b|\).

### Ejemplo de aplicación:
Demostrar que si \(3 \mid (a+b)\) y \(3 \mid (a-b)\), entonces \(3 \mid a\) y \(3 \mid b\).  
Sumando: \(3 \mid (a+b)+(a-b) = 2a\). Como \(3\) no divide a \(2\), necesitamos usar combinación:  
También \((a+b) - (a-b) = 2b\) ⇒ \(3 \mid 2b\). Luego \(3 \mid a\) y \(3 \mid b\) porque \(mcd(3,2)=1\) (propiedad que veremos más adelante).

---

## 4. Representación de Números no Divisibles respecto a un Módulo

Cuando un número no es divisible por otro, la división entera nos deja un **residuo** o **resto**. Este concepto es fundamental para entender las **congruencias**.

### Algoritmo de la División
Dados dos enteros \(D\) (dividendo) y \(d \neq 0\) (divisor), existen únicos enteros \(q\) (cociente) y \(r\) (residuo) tales que:
\[
D = d \cdot q + r, \quad \text{con } 0 \le r < |d|
\]
Si \(r = 0\) entonces \(d \mid D\); si \(r \neq 0\) entonces \(d \nmid D\).

### Representación por clases de residuo
Fijado un módulo \(m > 0\), cualquier entero \(N\) puede escribirse de una única forma como:
\[
N = m \cdot q + r, \quad r \in \{0, 1, 2, \dots, m-1\}
\]
El número \(r\) se llama **residuo** de \(N\) al dividirlo por \(m\).

Decimos que dos números son **congruentes módulo \(m\)** si tienen el mismo residuo:
\[
a \equiv b \pmod{m} \iff m \mid (a-b)
\]

### Ejemplo:
Tomemos módulo \(5\). Los números se clasifican en 5 clases según su residuo:
- Residuo 0: ..., -10, -5, 0, 5, 10, ... (múltiplos de 5)
- Residuo 1: ..., -9, -4, 1, 6, 11, ...
- Residuo 2: ..., -8, -3, 2, 7, 12, ...
- Residuo 3: ..., -7, -2, 3, 8, 13, ...
- Residuo 4: ..., -6, -1, 4, 9, 14, ...

Así, \(13 \equiv 3 \pmod{5}\) porque \(13 - 3 = 10\) es múltiplo de 5.

### Representación de números no divisibles
Un número no divisible por \(d\) se expresa como \(N = d \cdot q + r\) con \(1 \le r \le d-1\). Por ejemplo, los números que no son divisibles por 3 son de la forma \(3q+1\) o \(3q+2\).

#### Aplicación práctica:
Demuestra que ningún cuadrado perfecto puede terminar en 2, 3, 7 u 8.  
Basta analizar residuos módulo 10: cualquier entero \(n\) tiene residuo \(r \in \{0,...,9\}\) y \(n^2 \equiv r^2 \pmod{10}\). Calculando:
- \(0^2=0\), \(1^2=1\), \(2^2=4\), \(3^2=9\), \(4^2=6\), \(5^2=5\), \(6^2=6\), \(7^2=9\), \(8^2=4\), \(9^2=1\).  
Los residuos posibles son \(\{0,1,4,5,6,9\}\). Por tanto, nunca 2,3,7,8.

---

## 5. Criterios de Divisibilidad

Los criterios nos permiten saber si un número es divisible por otro sin realizar la división completa, observando sus cifras.

### Criterio para el 2
Un número es divisible por 2 si su última cifra es par (0,2,4,6,8).

### Criterio para el 3
Un número es divisible por 3 si la suma de sus cifras es múltiplo de 3.

### Criterio para el 4
Un número es divisible por 4 si el número formado por sus dos últimas cifras es múltiplo de 4.

### Criterio para el 5
Un número es divisible por 5 si termina en 0 o 5.

### Criterio para el 6
Debe ser divisible por 2 y por 3 (es decir, terminar en par y suma de cifras múltiplo de 3).

### Criterio para el 7 (algo más complejo)
Método: Separar la última cifra, duplicarla y restarla del número sin esa cifra. Repetir hasta obtener un número pequeño. Si ese número es múltiplo de 7, el original también.  
Ejemplo: 343 → 34 - 2×3 = 34 - 6 = 28, que es múltiplo de 7 → 343 es múltiplo de 7.

### Criterio para el 8
Un número es divisible por 8 si el número formado por sus tres últimas cifras es múltiplo de 8.

### Criterio para el 9
Un número es divisible por 9 si la suma de sus cifras es múltiplo de 9.

### Criterio para el 10
Termina en 0.

### Criterio para el 11
Se suman las cifras en posición impar (empezando desde la derecha) y las de posición par; la diferencia (impar - par) debe ser 0 o múltiplo de 11.  
Ejemplo: 121 → cifras impares: 1 (unidades) + 1 (centenas) = 2; pares: 2 (decenas). Diferencia = 0 → divisible.

### Justificación algebraica del criterio del 3:
Todo número \(N = a_n a_{n-1} \dots a_0\) (en decimal) se escribe como:
\[
N = a_n \cdot 10^n + a_{n-1} \cdot 10^{n-1} + \dots + a_0
\]
Como \(10 \equiv 1 \pmod{3}\), entonces \(10^k \equiv 1^k = 1 \pmod{3}\). Por tanto:
\[
N \equiv a_n + a_{n-1} + \dots + a_0 \pmod{3}
\]
Así, \(N\) es divisible por 3 si y solo si la suma de cifras lo es.

### Tabla resumen de criterios comunes:

| Divisor | Criterio                                 | Ejemplo                           |
|---------|------------------------------------------|-----------------------------------|
| 2       | Última cifra par                         | 238 → sí, 239 → no                |
| 3       | Suma de cifras múltiplo de 3             | 471 → 4+7+1=12 → sí               |
| 4       | Dos últimas cifras múltiplo de 4         | 732 → 32 es múltiplo de 4 → sí    |
| 5       | Termina en 0 o 5                         | 145 → sí, 147 → no                |
| 6       | Par y suma múltiplo de 3                 | 432 → par y 4+3+2=9 → sí          |
| 7       | Restar el doble de la última cifra       | 161 → 16-2=14 → sí                |
| 8       | Tres últimas cifras múltiplo de 8        | 5240 → 240 ÷ 8 = 30 → sí          |
| 9       | Suma de cifras múltiplo de 9             | 981 → 9+8+1=18 → sí               |
| 10      | Termina en 0                             | 230 → sí, 235 → no                |
| 11      | Diferencia (suma impares - suma pares) múltiplo de 11 | 2728 → (8+7)-(2+2)=15-4=11 → sí |

---

## 6. Problemas Resueltos (Ejemplos integradores)

### Problema 1 (Multiplicidad)
Halla el menor número positivo que sea múltiplo de 7 y al dividirlo entre 5 dé resto 3.

**Solución:**  
Buscamos \(N = 7k\) y \(N \equiv 3 \pmod{5}\).  
Los múltiplos de 7: 7,14,21,28,35,...  
Residuos mód 5: 2,4,1,3,0,... El primero con residuo 3 es 28.  
Respuesta: 28.

### Problema 2 (Criterio de divisibilidad)
¿Es 987654321 divisible por 9?  
Suma de cifras: 9+8+7+6+5+4+3+2+1 = 45, 45 es múltiplo de 9 → sí es divisible.

### Problema 3 (Representación con residuos)
Demuestra que \(n(n+1)(n+2)\) siempre es divisible por 6 para cualquier entero \(n\).

**Solución:**  
Entre tres enteros consecutivos hay al menos un múltiplo de 2 y exactamente un múltiplo de 3. Por tanto el producto es divisible por \(2 \cdot 3 = 6\).

---

## 7. Ejercicios Propuestos (para practicar)

1. Escribe todos los números de dos cifras que sean múltiplos de 7 y terminen en 4.
2. ¿Cuál es el residuo de \(2^{100}\) al dividirlo por 5? (Usa congruencias)
3. Aplica el criterio del 7 para verificar si 1078 es divisible por 7.
4. Encuentra un número de 4 cifras que sea divisible por 11 y por 3, pero no por 2.
5. Demuestra que si \(a \equiv b \pmod{m}\) y \(c \equiv d \pmod{m}\), entonces \(ac \equiv bd \pmod{m}\).

---

## 8. Conclusión de la Semana 5

Hemos cubierto los fundamentos de la divisibilidad: el concepto de múltiplo y divisor, las propiedades básicas, la representación de números mediante residuos (congruencias) y los criterios prácticos para detectar divisores pequeños. Estos conocimientos son la base para temas posteriores como ecuaciones diofánticas, MCD, MCM y números primos.
