# Semana 3: Teoría de Numeración

## Introducción

La **Teoría de Numeración** estudia los sistemas que utilizamos para representar los números, las reglas que los gobiernan y cómo convertir entre distintas bases. Comprender este tema es fundamental para la aritmética, la computación y la teoría de números.

En esta semana aprenderemos:

- Qué es un sistema de numeración y sus elementos.
- Propiedades fundamentales (teorema de representación, valor posicional).
- Casos especiales de cambio de base (incluyendo bases no decimales).
- Operaciones aritméticas en diferentes bases.

---

## 1. Sistema de Numeración

### 1.1 Definición básica

Un **sistema de numeración** es un conjunto de símbolos (cifras o dígitos) y reglas que permiten representar cantidades de manera única.

Todo sistema se define por su **base** (\(b\)), que es un número natural mayor o igual a 2. La base indica cuántos símbolos distintos se usan.

- **Base 10 (decimal)**: símbolos \(0,1,2,3,4,5,6,7,8,9\).
- **Base 2 (binario)**: símbolos \(0,1\).
- **Base 16 (hexadecimal)**: símbolos \(0-9, A, B, C, D, E, F\).

### 1.2 Representación polinómica

En un sistema de base \(b\), cualquier número \(N\) se escribe como:

\[
N = (a_n a_{n-1} \dots a_1 a_0)_{b}
\]

donde cada \(a_i\) es un dígito válido (\(0 \le a_i \le b-1\)) y \(a_n \neq 0\).

El **valor** de \(N\) se obtiene mediante el **teorema de representación**:

\[
N = a_n \cdot b^n + a_{n-1} \cdot b^{n-1} + \dots + a_1 \cdot b^1 + a_0 \cdot b^0
\]

**Ejemplo básico (decimal):**  
\(375_{10} = 3\cdot10^2 + 7\cdot10^1 + 5\cdot10^0\)

**Ejemplo binario:**  
\(1011_2 = 1\cdot2^3 + 0\cdot2^2 + 1\cdot2^1 + 1\cdot2^0 = 8+0+2+1 = 11_{10}\)

**Ejemplo base 5:**  
\(243_5 = 2\cdot5^2 + 4\cdot5^1 + 3\cdot5^0 = 2\cdot25 + 4\cdot5 + 3 = 50+20+3 = 73_{10}\)

---

## 2. Propiedades del Sistema de Numeración

### 2.1 Propiedad de unicidad
Cada número tiene una única representación en una base dada (salvo ceros a la izquierda).

### 2.2 Propiedad de orden
Para comparar números en la misma base, se comparan de izquierda a derecha (dígito más significativo primero).

### 2.3 Teorema de cambio de base
Dado un número en base \(b_1\), existe un único número en base \(b_2\) que representa la misma cantidad.

### 2.4 Número de cifras necesarias
Para representar un número \(N\) en base \(b\), el número de dígitos necesarios es:

\[
k = \lfloor \log_b N \rfloor + 1
\]

**Ejemplo:** \(N=100\) en base 10 → \(k = \lfloor \log_{10}100 \rfloor + 1 = 2+1=3\) dígitos.  
En base 2 → \(k = \lfloor \log_2 100 \rfloor + 1 = \lfloor 6.64 \rfloor + 1 = 6+1=7\) dígitos (\(1100100_2\)).

### 2.5 Relación entre bases que son potencias
Si \(b_2 = b_1^k\), la conversión es directa agrupando dígitos.

Ejemplo: Binario a octal (base 8 = \(2^3\)):  
\(101101_2\) se agrupa de derecha a izquierda en grupos de 3 bits: \(101\;101_2 = 55_8\).

---

## 3. Cambio de Base (Casos Generales)

### 3.1 De base \(b\) a base 10 (método polinómico)

Se evalúa el polinomio mediante multiplicaciones sucesivas (método de Horner para mayor eficiencia).

**Ejemplo:** Convertir \(321_4\) a decimal.  
\(321_4 = 3\cdot4^2 + 2\cdot4^1 + 1\cdot4^0 = 3\cdot16 + 2\cdot4 + 1 = 48+8+1 = 57_{10}\)

### 3.2 De base 10 a base \(b\) (método de divisiones sucesivas)

Se divide el número decimal entre la base \(b\) repetidamente, los residuos (leídos del último al primero) forman el número en base \(b\).

**Ejemplo:** Convertir \(57_{10}\) a base 4.

\[
\begin{array}{rcl}
57 \div 4 &=& 14 \text{ residuo } 1 \\
14 \div 4 &=& 3 \text{ residuo } 2 \\
3 \div 4 &=& 0 \text{ residuo } 3
\end{array}
\]

Leyendo residuos de abajo arriba: \(321_4\).  
Comprobación: ya vimos que \(321_4 = 57_{10}\).

### 3.3 Entre dos bases cualesquiera (ruta decimal)

Para convertir de base \(a\) a base \(b\) (ambas distintas de 10), primero se pasa a base 10 (método polinómico) y luego de base 10 a base \(b\) (divisiones sucesivas).

**Ejemplo:** Convertir \(211_3\) a base 5.

- Paso 1: \(211_3 = 2\cdot3^2+1\cdot3^1+1\cdot3^0 = 18+3+1=22_{10}\).
- Paso 2: \(22\) a base 5:  
  \(22 \div 5 = 4\) residuo \(2\)  
  \(4 \div 5 = 0\) residuo \(4\)  
  → \(42_5\).

Resultado: \(211_3 = 42_5\).

---

## 4. Casos Especiales de Cambio de Base

### 4.1 Bases que son potencias de una misma base

Si \(B = b^k\), la conversión se hace agrupando dígitos de \(b\) en grupos de \(k\).

- **Binario a octal** (\(2^3=8\)): grupos de 3 bits.  
  \(1101011_2\) → añadir ceros a izquierda: \(001\;101\;011_2 = 153_8\).

- **Binario a hexadecimal** (\(2^4=16\)): grupos de 4 bits.  
  \(1101011_2\) → \(0110\;1011_2 = 6B_{16}\).

- **Octal a binario**: cada dígito octal se expande a 3 bits.  
  \(153_8 = 001\;101\;011_2 = 1101011_2\).

### 4.2 Números con parte fraccionaria

Para la parte fraccionaria en base \(b\) a decimal:

\[
(0.a_1 a_2 \dots)_b = a_1 b^{-1} + a_2 b^{-2} + \dots
\]

**Ejemplo:** \(0.21_3 = 2\cdot3^{-1}+1\cdot3^{-2} = \frac{2}{3}+\frac{1}{9} = \frac{7}{9} \approx 0.777..._{10}\)

De decimal a base \(b\) (parte fraccionaria): multiplicaciones sucesivas por \(b\).

**Ejemplo:** Convertir \(0.625_{10}\) a binario.

\[
0.625 \times 2 = 1.250 \quad \text{parte entera } 1 \\
0.250 \times 2 = 0.500 \quad \text{parte entera } 0 \\
0.500 \times 2 = 1.000 \quad \text{parte entera } 1
\]

Resultado: \(0.101_2\).  
Comprobación: \(0.101_2 = 1\cdot2^{-1}+0\cdot2^{-2}+1\cdot2^{-3} = 0.5+0.125=0.625\).

### 4.3 Conversión de fracciones periódicas entre bases

Una fracción que es periódica en una base puede ser exacta o periódica en otra. Se usa el método de multiplicación por potencias de la base para hallar la fracción generatriz.

**Ejemplo:** Convertir \(0.\overline{12}_3\) a base 10.

Sea \(x = 0.121212..._3\). Multiplicamos por \(3^2 = 9\) (base 3):

\[
9x = 12.121212..._3 = 12_3 + x
\]

Pero \(12_3 = 1\cdot3+2=5_{10}\).  
Entonces \(9x = 5 + x\) → \(8x=5\) → \(x = \frac{5}{8} = 0.625_{10}\).

---

## 5. Operaciones en Sistemas de Numeración

### 5.1 Suma y resta en cualquier base

Se opera dígito a dígito de derecha a izquierda, acarreando cuando la suma alcanza o supera la base.

**Ejemplo suma en base 5:** \(234_5 + 143_5\)

\[
\begin{array}{cccc}
 & 2 & 3 & 4_5 \\
+ & 1 & 4 & 3_5 \\
\hline
\end{array}
\]

- Unidades: \(4+3=7\) en decimal. \(7\) en base 5 es \(12_5\) → escribo 2, llevo 1.
- Quintos: \(3+4+1\) (acarreo) = \(8\). \(8\) en base 5 = \(13_5\) → escribo 3, llevo 1.
- Veinticinco: \(2+1+1=4\) → escribo 4.

Resultado: \(432_5\).  
Comprobación: \(234_5=2\cdot25+3\cdot5+4=69_{10}\); \(143_5=1\cdot25+4\cdot5+3=48_{10}\); suma \(117_{10}\) y \(432_5=4\cdot25+3\cdot5+2=100+15+2=117_{10}\).

**Ejemplo resta en base 4:** \(321_4 - 133_4\)

\[
\begin{array}{cccc}
 & 3 & 2 & 1_4 \\
- & 1 & 3 & 3_4 \\
\hline
\end{array}
\]

- Unidades: \(1-3\) no puede → pedimos prestado 1 grupo de 4 al dígito de la izquierda: \(1+4=5\), \(5-3=2\). El dígito de las cuartos (2) se reduce a 1.
- Cuartos: ahora tenemos \(1-3\) → no puede, pedimos prestado al de 16: \(1+4=5\), \(5-3=2\). El dígito de 16 (3) se reduce a 2.
- Dieciseisavos: \(2-1=1\).

Resultado: \(122_4\).  
Comprobación: \(321_4=57_{10}\), \(133_4=1\cdot16+3\cdot4+3=31_{10}\), diferencia \(26_{10}\); \(122_4=1\cdot16+2\cdot4+2=16+8+2=26\).

### 5.2 Multiplicación

Se multiplica cada dígito del multiplicador por el multiplicando, desplazando según posición, y luego se suman los productos parciales (en la misma base).

**Ejemplo base 3:** \(21_3 \times 12_3\)

- \(21_3 \times 2_3\):  
  \(1\times2=2\) (unidades), \(2\times2=4\) pero en base 3, \(4=11_3\) → escribo 1, llevo 1. Total: \(112_3\).
- \(21_3 \times 1_3\) (desplazado un lugar): \(21_3 \times 1_3 = 21_3\) seguido de un cero: \(210_3\).
- Sumar \(112_3 + 210_3\):  
  Unidades: \(2+0=2\); tríos: \(1+1=2\); nueves: \(1+2=3\) → \(3\) en base 3 = \(10_3\) → escribo 0, llevo 1; veintisietes: \(1\). Resultado: \(1022_3\).

Comprobación en decimal: \(21_3=7\), \(12_3=5\), producto \(35_{10}\). \(1022_3=1\cdot27+0\cdot9+2\cdot3+2=27+0+6+2=35\).

### 5.3 División

Similar a la división decimal, usando la tabla de multiplicar en la base correspondiente.

**Ejemplo base 6:** Dividir \(245_6\) entre \(5_6\).

- \(5 \times 3 = 15_6\) (pero \(15_6 = 1\cdot6+5=11_{10}\); comprobamos: \(5_6 \times 3_6 = 5\times3=15\) decimal = \(23_6\)? Mejor hacerlo sistemáticamente: en base 6, la tabla del 5: \(5\times1=5\), \(5\times2=14_6\) (porque \(10_{10}=14_6\)), \(5\times3=23_6\) (15 decimal = \(23_6\)), \(5\times4=32_6\) (20 decimal = \(32_6\)).  
  Buscamos cuántas veces cabe \(5_6\) en \(24_6\) (primeros dos dígitos). \(24_6 = 2\cdot6+4=16_{10}\); \(5_6=5_{10}\); \(16/5=3\) → probamos \(3\): \(5_6\times3_6 = 23_6\). Restamos: \(24_6 - 23_6 = 1_6\). Bajamos el siguiente dígito (5): queda \(15_6\). \(5_6\) cabe en \(15_6\) exactamente \(3\) veces? \(15_6=11_{10}\); \(11/5=2\) resto 1. Mejor: \(5_6\times2_6=14_6\), resta \(15_6-14_6=1_6\). Cociente final: \(32_6\) y residuo \(1_6\).

Verificación: \(32_6 \times 5_6 + 1_6 = (3\cdot6+2)\times5 + 1 = (20)\times5 +1 =101\) decimal. \(245_6=2\cdot36+4\cdot6+5=72+24+5=101\). Correcto.

---

## 6. Ejercicios Resueltos (Nivel Intermedio a Avanzado)

### Ejercicio 1
Convertir \(101011_2\) a base 4 (sin pasar por decimal).

**Solución:**  
Base 4 = \(2^2\), agrupamos bits de derecha a izquierda en grupos de 2:  
\(10\;10\;11_2\) = \(2\;2\;3_4\) → \(223_4\).

### Ejercicio 2
Hallar la base \(b\) si \(124_b = 62_{10}\).

**Solución:**  
\(124_b = 1\cdot b^2 + 2\cdot b + 4 = b^2+2b+4 = 62\) → \(b^2+2b-58=0\) → \(b = \frac{-2\pm\sqrt{4+232}}{2} = \frac{-2\pm\sqrt{236}}{2}\). \(\sqrt{236}\approx 15.36\), solución positiva \(b\approx 6.68\). No es entero → ¿error? Revisemos: \(b^2+2b+4=62\) → \(b^2+2b-58=0\), discriminante \(4+232=236\), no es cuadrado perfecto. Entonces no hay base entera? Pero el enunciado supone que sí. Comprobemos \(b=7\): \(124_7=1\cdot49+2\cdot7+4=49+14+4=67\), no 62. \(b=6\): \(124_6=1\cdot36+2\cdot6+4=36+12+4=52\). Ninguno da 62. Entonces la base no es entera? En problemas reales, a veces la base es mayor que el dígito más alto. Aquí el dígito 4 implica base ≥5. Probemos \(b=8\): \(124_8=64+16+4=84\). No hay solución entera. Entonces el número \(62_{10}\) no es representable como \(124_b\) con b entero. Es un ejercicio para detectar inconsistencia.

**Respuesta:** No existe base entera \(b\).

### Ejercicio 3 (Avanzado)
Demostrar que un número es divisible por \((b-1)\) si y solo si la suma de sus dígitos en base \(b\) es divisible por \((b-1)\).

**Solución (bosquejo):**  
Sea \(N = a_n b^n + \dots + a_0\). Como \(b \equiv 1 \pmod{b-1}\), entonces \(b^k \equiv 1 \pmod{b-1}\). Luego \(N \equiv a_n + a_{n-1} + \dots + a_0 \pmod{b-1}\). Por lo tanto \(N \equiv S \pmod{b-1}\), donde \(S\) es suma de dígitos. Así \(b-1 \mid N \iff b-1 \mid S\).  
*(Caso particular: criterio del 9 en decimal)*.

---

## 7. Resumen y Fórmulas Clave

| Concepto | Fórmula / Método |
|----------|------------------|
| Valor posicional | \(N = \sum a_i b^i\) |
| Decimal → base \(b\) | Divisiones sucesivas (residuos) |
| Base \(b\) → decimal | Evaluación polinómica |
| Bases potencia | Agrupación de dígitos |
| Suma/Resta | Acarreo cuando suma ≥ \(b\) |
| Multiplicación | Productos parciales en base \(b\) |
| División | Algoritmo estándar con tabla de multiplicar en base \(b\) |

---

## 8. Ejercicios Propuestos

1. Convertir \(110011_2\) a base 8 y a base 16.
2. Convertir \(A3F_{16}\) a base 2 y a base 8.
3. Sumar \(432_5 + 234_5\) y comprobar en decimal.
4. Restar \(1001_2 - 111_2\).
5. Multiplicar \(12_3 \times 21_3\).
6. Hallar la base \(b\) si \(25_b = 32_{10}\).
7. Demostrar que todo número en base \(b\) termina en cero si y solo si es múltiplo de \(b\).

---

## 9. Soluciones a Ejercicios Propuestos (Breves)

1. \(110011_2 = 63_8 = 33_{16}\)  
2. \(A3F_{16} = 101000111111_2 = 5077_8\)  
3. \(432_5+234_5 = 1221_5\) (comprobación: \(432_5=117, 234_5=69, suma=186; 1221_5=1\cdot125+2\cdot25+2\cdot5+1=125+50+10+1=186\))  
4. \(1001_2 - 111_2 = 10_2\) (9-7=2)  
5. \(12_3 \times 21_3 = 1012_3\) (5×7=35; \(1012_3=27+0+3+2=32\)? Revisar: 12_3=5, 21_3=7, producto 35. 1012_3=1·27+0·9+1·3+2=27+3+2=32 → error. Calculemos bien: 12_3 × 21_3 = (1·3+2)×(2·3+1)=5×7=35. 35 en base 3: 35÷3=11 r2, 11÷3=3 r2, 3÷3=1 r0, 1÷3=0 r1 → 1022_3. Sí, 1022_3=27+0+6+2=35. Respuesta corregida: 1022_3.)  
6. \(25_b = 2b+5 = 32 \Rightarrow 2b=27 \Rightarrow b=13.5\) → no entero. Revisar: si \(25_b\) significa dígitos 2 y 5, entonces b>5. 2b+5=32 → b=13.5. No es entero. Luego no hay base entera.  
7. Demostración: \(N = a_n b^n + \dots + a_1 b + a_0\). Termina en cero ⇔ \(a_0=0\) ⇔ \(N\) es múltiplo de \(b\).

---

Con esto concluye el temario completo de la Semana 3. Practica con los ejercicios y verifica tus respuestas. ¡La teoría de numeración es la base para entender sistemas digitales y teoría de números!