# Semana 3: Teoría de la Numeración

## 1. Sistema de Numeración

Un **sistema de numeración** es un conjunto de reglas y símbolos que permiten representar cantidades numéricas. Todo sistema se caracteriza por su **base**, que es un número entero positivo mayor o igual a 2.

### 1.1 Base de un sistema
La base indica cuántas unidades de un orden forman una unidad del orden inmediato superior. Los sistemas más comunes son:

| Base | Nombre          | Símbolos permitidos               |
|------|-----------------|-----------------------------------|
| 2    | Binario         | 0, 1                              |
| 8    | Octal           | 0,1,2,3,4,5,6,7                   |
| 10   | Decimal         | 0,1,2,3,4,5,6,7,8,9               |
| 16   | Hexadecimal     | 0-9 y A=10, B=11, C=12, D=13, E=14, F=15 |

### 1.2 Teorema fundamental de la numeración
Todo número \( N \) en base \( b \) se puede expresar como un polinomio en potencias de \( b \):

\[
N_{(b)} = a_n a_{n-1} \dots a_1 a_0 \; (b)
\]

Donde \( a_i \) son dígitos (\( 0 \le a_i < b \)) y su valor es:

\[
N = a_n \cdot b^n + a_{n-1} \cdot b^{n-1} + \dots + a_1 \cdot b^1 + a_0 \cdot b^0
\]

#### Ejemplo:
El número \( 342_{(5)} \) (base 5) equivale en decimal a:

\[
342_{(5)} = 3 \cdot 5^2 + 4 \cdot 5^1 + 2 \cdot 5^0 = 3\cdot 25 + 4\cdot 5 + 2\cdot 1 = 75 + 20 + 2 = 97_{(10)}
\]

## 2. Propiedades del Sistema de Numeración

### 2.1 Propiedad fundamental
En cualquier base \( b \), el mayor número que se puede representar con \( n \) dígitos es \( b^n - 1 \).  
El menor número con \( n \) dígitos es \( b^{n-1} \) (si el primer dígito es 1 y los demás 0).

#### Ejemplo:
En base 5, con 3 dígitos:
- Mayor: \( 444_{(5)} = 4\cdot5^2 + 4\cdot5 + 4 = 124_{(10)} \), que es \( 5^3 - 1 = 124 \).
- Menor: \( 100_{(5)} = 1\cdot5^2 = 25_{(10)} = 5^{3-1} \).

### 2.2 Cambio de base
#### a) De base \( b \) a decimal (método polinómico)
Ya visto en el teorema fundamental.

#### b) De decimal a base \( b \) (divisiones sucesivas)
Se divide el número decimal entre \( b \) repetidamente, y los restos leídos en orden inverso dan el número en base \( b \).

#### Ejemplo:
Convertir \( 58_{(10)} \) a base 6.

\[
\begin{array}{r|l}
58 & 6 \\
4  & 9 \\
   & --- \\
    & 9 & 6 \\
    & 3 & 1 \\
      &   & 1
\end{array}
\]

Restos (de abajo arriba): 1, 3, 4 → \( 58_{(10)} = 134_{(6)} \)

### 2.3 Representación de números en diferentes bases
Un número puede tener varias representaciones si cambiamos la base. Se cumple que:

\[
N_{(b)} = N_{(10)} = N_{(c)} \quad \text{(valor numérico igual, distinta escritura)}
\]

## 3. Casos Especiales de Cambio de Base

### 3.1 Bases que son potencias de otra
Si \( b = c^k \), la conversión entre ambas es directa agrupando dígitos.

- **De binario (base 2) a octal (base 8)**: Como \( 8 = 2^3 \), se agrupan los bits de 3 en 3 desde la derecha.
- **De binario a hexadecimal (base 16)**: \( 16 = 2^4 \), agrupar de 4 en 4.

#### Ejemplo:
\( 10110111_{(2)} \) a octal:
Agrupamos: 010 110 111 → 2 6 7 → \( 267_{(8)} \)

### 3.2 Números con parte fraccionaria
Se aplica el mismo principio: la parte fraccionaria se multiplica por la base sucesivamente.

#### Ejemplo:
Convertir \( 0.625_{(10)} \) a binario:

\[
0.625 \times 2 = 1.250 \quad (\text{parte entera } 1)\\
0.250 \times 2 = 0.500 \quad (\text{parte entera } 0)\\
0.500 \times 2 = 1.000 \quad (\text{parte entera } 1)
\]

Tomando las partes enteras en orden: \( 0.625_{(10)} = 0.101_{(2)} \)

### 3.3 Base no entera o negativa (teórico)
No son habituales en cursos básicos, pero existen sistemas con base negativa o fraccionaria (p. ej. base -2). No se ven en este nivel.

## 4. Operaciones en Sistemas de Numeración

### 4.1 Suma
Se suma dígito a dígito de derecha a izquierda. Si la suma excede \( b-1 \), se resta \( b \) y se lleva 1 al siguiente orden.

#### Ejemplo:
Sumar \( 345_{(6)} + 432_{(6)} \)

\[
\begin{array}{cccc}
 & 3 & 4 & 5_{(6)} \\
+ & 4 & 3 & 2_{(6)} \\
\hline
 & 1 & 2 & 1 \\
\end{array}
\]
- 5+2 = 7, como 7≥6 → 7-6=1, llevo 1.
- 4+3+1(llevada)=8 → 8-6=2, llevo 1.
- 3+4+1=8 → 8-6=2, llevo 1 (que pasa a cuarto dígito).

Resultado: \( 1221_{(6)} \)

### 4.2 Resta
Se resta dígito a dígito. Si el minuendo es menor que el sustraendo, se pide prestado 1 del orden superior, que equivale a \( b \) unidades.

#### Ejemplo:
\( 512_{(8)} - 347_{(8)} \)

\[
\begin{array}{cccc}
 & 5 & 1 & 2_{(8)} \\
- & 3 & 4 & 7_{(8)} \\
\hline
 & 1 & 4 & 3_{(8)} \\
\end{array}
\]
- 2 < 7 → prestamos 1 de la siguiente columna: 2+8=10, 10-7=3.
- El 1 se convierte en 0, pero tenía prestado? Mejor hacerlo paso a paso:  
  Unidad: 2 - 7 no puede, prestamos 1 de la columna de 8¹: 12(8) - 7 = (10 en decimal) 10-7=3, y esa columna queda 0 (porque 1 se fue).  
  Luego columna 8¹: 0 - 4 no puede, prestamos de la columna 8²: (0+8) - 4 = 4, y la columna 8² pasa de 5 a 4.  
  Columna 8²: 4 - 3 = 1. Resultado: 143.

### 4.3 Multiplicación
Se multiplica cada dígito del multiplicador por el multiplicando, igual que en decimal, pero llevando cuando el producto parcial excede \( b-1 \).

#### Ejemplo:
\( 23_{(4)} \times 12_{(4)} \)

Primero \( 23 \times 2 \):  
- 3×2=6 → 6-4=2 llevo 1 → 2×2+1=5 → 5-4=1 llevo 1 → resultado parcial \( 112_{(4)} \).

Luego \( 23 \times 1 \) (pero es 1×4¹, o sea desplazado): da \( 23_{(4)} \) (en realidad 23×1=23, pero como es el segundo dígito se corre un lugar).

Sumamos:  
\[
112_{(4)} + 230_{(4)} = 1002_{(4)}
\]
(Verificación: 23₄ = 11₁₀, 12₄ = 6₁₀, producto 66₁₀ = 1002₄ porque 1×64+0×16+0×4+2=66)

### 4.4 División
Similar al decimal, pero usando la tabla de multiplicar en la base dada.

#### Ejemplo:
Dividir \( 134_{(5)} \) entre \( 4_{(5)} \).

- \( 4 \times 2 = 8 \) (en decimal) → en base 5: 13₅ = 8₁₀, cabe 2.  
  2×4=13₅ (porque 2×4=8=1×5+3), resto 0.  
  Bajo el 4: queda 4 entre 4 = 1, resto 0.  
  Cociente \( 21_{(5)} \).

## 5. Ejercicios Resueltos (Casos Especiales)

### Ejercicio 1:
Convertir \( 1011011_{(2)} \) a base 10.

\[
1\cdot2^6 + 0\cdot2^5 + 1\cdot2^4 + 1\cdot2^3 + 0\cdot2^2 + 1\cdot2^1 + 1\cdot2^0 = 64+0+16+8+0+2+1 = 91
\]

### Ejercicio 2:
¿Cuál es el mayor número de 3 dígitos en base 7? Dar su equivalente decimal.

El mayor es \( 666_{(7)} = 6\cdot49 + 6\cdot7 + 6 = 294+42+6 = 342_{(10)} \). También \( 7^3-1 = 343-1 = 342 \).

### Ejercicio 3:
Si \( 123_{(b)} = 51_{(10)} \), hallar b.

\[
1\cdot b^2 + 2\cdot b + 3 = 51 \Rightarrow b^2 + 2b - 48 = 0
\]
\[
b = \frac{-2 \pm \sqrt{4+192}}{2} = \frac{-2 \pm 14}{2} \Rightarrow b = 6 \quad (\text{positivo})
\]

### Ejercicio 4:
Efectuar \( 345_{(6)} + 235_{(6)} \) y expresar en base 6.

\[
5+5=10 → 10-6=4, llevo 1.\\
4+3+1=8 → 8-6=2, llevo 1.\\
3+2+1=6 → 6-6=0, llevo 1.\\
Resultado: 1024_{(6)}
\]

## 6. Resumen de Fórmulas Útiles

- Descomposición polinómica: \( N = \sum_{i=0}^{n} a_i b^i \)
- Cambio de decimal a base \( b \): divisiones sucesivas.
- Número de dígitos de \( N \) en base \( b \): \( \lfloor \log_b N \rfloor + 1 \)
- Relación entre bases potencia: \( b = c^k \) → agrupación de dígitos.

## 7. Ejercicios Propuestos

1. Convertir \( 101010_{(2)} \) a decimal, octal y hexadecimal.
2. Hallar la base \( b \) si \( 212_{(b)} = 35_{(10)} \).
3. Sumar \( 777_{(8)} + 1_{(8)} \) y dar el resultado en base 8.
4. Multiplicar \( 34_{(5)} \times 12_{(5)} \).
5. ¿Cuántos dígitos tiene el número \( 3^{100} \) en base 3?

---

> **Nota:** Este material cubre completamente el contenido de la Semana 3 del temario de Aritmética para Ingenierías (Ciclo Marzo-Julio 2026).