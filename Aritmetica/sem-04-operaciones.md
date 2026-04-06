# Semana 4: Operaciones Fundamentales

## Introducción

Las **operaciones fundamentales** de la aritmética son la base de casi todos los cálculos matemáticos. En esta semana estudiaremos la **adición**, **sustracción**, **multiplicación** y **división** aplicadas a números naturales y enteros positivos, aunque extenderemos algunos conceptos a los enteros en general.

Dominar estas operaciones no solo implica saber ejecutar algoritmos, sino comprender sus propiedades, relaciones y aplicaciones en problemas cotidianos y teóricos.

---

## 1. Adición (Suma)

### Definición
La adición es la operación que consiste en **agrupar** dos o más cantidades (sumandos) para obtener una cantidad total llamada **suma** o **total**.

$$a + b = c$$

donde $a$ y $b$ son los **sumandos** y $c$ es la **suma**.

### Propiedades de la suma (en $\mathbb{N}$ y $\mathbb{Z}$)

| Propiedad | Expresión | Ejemplo |
|-----------|-----------|---------|
| **Conmutativa** | $a + b = b + a$ | $5 + 3 = 3 + 5 = 8$ |
| **Asociativa** | $(a + b) + c = a + (b + c)$ | $(2+3)+4 = 2+(3+4) = 9$ |
| **Elemento neutro** | $a + 0 = a$ | $7 + 0 = 7$ |
| **Elemento opuesto** (en $\mathbb{Z}$) | $a + (-a) = 0$ | $5 + (-5) = 0$ |

> En $\mathbb{N}$ no existe elemento opuesto (números negativos).

### Algoritmo de la suma (con acarreo)

Para sumar números de varias cifras:

1. Colocar los números uno debajo del otro alineando las unidades.
2. Sumar columna por columna de derecha a izquierda.
3. Si la suma parcial es $\ge 10$, se escribe la cifra de las unidades y se "lleva" la decena a la columna siguiente.

**Ejemplo paso a paso:** $345 + 287$
3 4 5

2 8 7


- Unidades: $5+7=12$, escribo $2$, llevo $1$.
- Decenas: $4+8+1=13$, escribo $3$, llevo $1$.
- Centenas: $3+2+1=6$, escribo $6$.

Resultado: $632$

### Propiedades avanzadas

- **Suma de una progresión aritmética**: $1+2+\cdots+n = \frac{n(n+1)}{2}$
- **Suma de números pares**: $2+4+6+\cdots+2n = n(n+1)$
- **Suma de impares**: $1+3+5+\cdots+(2n-1)=n^2$

---

## 2. Sustracción (Resta)

### Definición
La sustracción es la operación inversa de la adición. Dados dos números $a$ (minuendo) y $b$ (sustraendo), la resta busca un número $c$ (diferencia) tal que:

$$a - b = c \quad \Longleftrightarrow \quad b + c = a$$

### Algoritmo de la resta con "préstamo" (o reagrupación)

Cuando una cifra del minuendo es menor que la correspondiente del sustraendo, se "pide" una unidad a la cifra de la izquierda.

**Ejemplo:** $432 - 187$
4 3 2

1 8 7

- Unidades: $2 < 7$, tomo $1$ decena de las $3$ decenas → $12 - 7 = 5$. Quedan $2$ decenas.
- Decenas: $2 < 8$, tomo $1$ centena de las $4$ centenas → $12 - 8 = 4$. Quedan $3$ centenas.
- Centenas: $3 - 1 = 2$.

Resultado: $245$

### Propiedades importantes

- **No es conmutativa**: $a-b \neq b-a$ (excepto si $a=b$).
- **No es asociativa**: $(a-b)-c \neq a-(b-c)$ en general.
- **Elemento neutro**: $a - 0 = a$.
- **Resta de un número negativo**: $a - (-b) = a+b$.

### Complementos y aplicaciones

**Complemento aritmético** de un número $n$ respecto a una potencia de $10$: es la diferencia entre $10^k$ y $n$. Útil para restar usando sumas.

Ejemplo: Para calcular $1234 - 567$, podemos usar complemento a 1000 de 567 = 433, sumar a 1234? No es directo, pero es la base de la resta con complemento en computadoras.

---

## 3. Multiplicación

### Definición
La multiplicación es una suma abreviada de sumandos iguales:

$$a \times b = \underbrace{a + a + \cdots + a}_{b \text{ veces}}$$

$a$ es el **multiplicando**, $b$ el **multiplicador** y el resultado se llama **producto**.

### Propiedades de la multiplicación

| Propiedad | Expresión | Ejemplo |
|-----------|-----------|---------|
| Conmutativa | $a \cdot b = b \cdot a$ | $4 \cdot 7 = 7 \cdot 4 = 28$ |
| Asociativa | $(a \cdot b) \cdot c = a \cdot (b \cdot c)$ | $(2\cdot3)\cdot4=2\cdot(3\cdot4)=24$ |
| Distributiva respecto a la suma | $a \cdot (b+c) = a \cdot b + a \cdot c$ | $3\cdot(4+5)=3\cdot4+3\cdot5=27$ |
| Elemento neutro | $a \cdot 1 = a$ | $9 \cdot 1 = 9$ |
| Elemento absorbente | $a \cdot 0 = 0$ | $7 \cdot 0 = 0$ |

### Algoritmos de multiplicación

#### Multiplicación por una cifra
Se multiplica cada cifra del multiplicando por el multiplicador, llevando acarreo.

Ejemplo: $234 \times 6$

- $6\times4=24$ → pongo $4$, llevo $2$
- $6\times3=18+2=20$ → pongo $0$, llevo $2$
- $6\times2=12+2=14$ → resultado $1404$

#### Multiplicación por varias cifras
Se multiplica el multiplicando por cada cifra del multiplicador, desplazando los resultados parciales (productos parciales) y luego se suman.

**Ejemplo:** $345 \times 27$
3 4 5
× 2 7

2 4 1 5 (345 × 7)

6 9 0 (345 × 2, desplazado una posición)

9 3 1 5


#### Método de la celosía (o lattice) - alternativa visual

Se dibuja una cuadrícula, se colocan los dígitos y se suman diagonales. Es útil para entender el algoritmo.

### Multiplicaciones rápidas y trucos

- **Multiplicar por 9**: $a \times 9 = a \times (10-1) = 10a - a$.
- **Multiplicar por 11**: Para números de dos cifras, $ab \times 11 = a(a+b)b$ (si $a+b<10$). Ej: $34\times11=374$ (porque $3+4=7$).
- **Cuadrado de un número terminado en 5**: $(10n+5)^2 = 100n(n+1)+25$. Ej: $65^2 = 100\cdot6\cdot7+25 = 4200+25=4225$.

---

## 4. División

### Definición
La división es la operación inversa de la multiplicación. Dados dos números $D$ (dividendo) y $d$ (divisor, $d \neq 0$), se buscan dos números $q$ (cociente) y $r$ (residuo) tales que:

$$D = d \cdot q + r, \quad \text{con } 0 \le r < d$$

Si $r=0$, la división es **exacta**; si $r>0$, es **inexacta**.

### Algoritmo de la división (método tradicional)

**Ejemplo:** Dividir $846$ entre $7$

1. Tomamos las primeras cifras del dividendo que sean mayores o iguales al divisor: $8 \ge 7$.
2. $8 \div 7 = 1$ (cociente parcial). $1\times7=7$, resto $8-7=1$.
3. Bajamos la siguiente cifra (4) → $14$.
4. $14 \div 7 = 2$, $2\times7=14$, resto $0$.
5. Bajamos la siguiente cifra (6) → $6$.
6. $6 \div 7 = 0$, resto $6$.
7. Cociente final $120$, residuo $6$. Verificación: $7\times120+6=840+6=846$.

### División larga con decimales

Si se desea obtener un cociente decimal, se añade un punto decimal al cociente y se agregan ceros al residuo.

Ejemplo: $7 \div 2 = 3.5$

### Propiedades de la división (en $\mathbb{Z}$)

- **No es conmutativa**: $a/b \neq b/a$ en general.
- **Distributiva solo por la derecha**: $(a+b)/c = a/c + b/c$ (si $c\neq0$). Pero $c/(a+b) \neq c/a + c/b$.
- **División exacta**: $d$ divide a $D$ si $D \bmod d = 0$. Se denota $d \mid D$.
- **Residuo de una suma**: $(a+b) \bmod m = ((a \bmod m)+(b \bmod m)) \bmod m$.

### Algoritmo de la división sintética (para polinomios) no es tema, pero en aritmética podemos usar la **división por factores**:

Ejemplo: $345 \div 15 = 345 \div (3\times5) = (345\div3)\div5 = 115\div5=23$.

### Criterios de divisibilidad (repaso breve)

| Divisor | Criterio | Ejemplo |
|---------|----------|---------|
| 2 | Última cifra par | 124 sí |
| 3 | Suma de cifras múltiplo de 3 | 123: 1+2+3=6 → sí |
| 4 | Dos últimas cifras múltiplo de 4 | 316: 16 sí |
| 5 | Termina en 0 o 5 | 130 sí |
| 9 | Suma de cifras múltiplo de 9 | 189: 1+8+9=18 → sí |
| 10 | Termina en 0 | 450 sí |

---

## 5. Relación entre las operaciones y jerarquía

Cuando combinamos varias operaciones, se debe respetar la **jerarquía** (orden de operaciones):

1. **Paréntesis** (de más interno a externo)
2. **Potenciación y radicación** (no son tema de esta semana pero aparecen)
3. **Multiplicación y división** (de izquierda a derecha)
4. **Adición y sustracción** (de izquierda a derecha)

Regla nemotécnica: **PEMDAS** (Paréntesis, Exponentes, Multiplicación/División, Adición/Sustracción) o **PAPOMUDAS** en español.

**Ejemplo:** $3 + 4 \times 2 - (6 \div 3) = 3 + 8 - 2 = 9$

> **Atención:** la multiplicación tiene prioridad sobre la suma, a menos que haya paréntesis.

---

## 6. Problemas resueltos

### Problema 1 (Suma y resta combinadas)
Un comerciante tiene en su caja \$1250. Recibe un pago de \$345 y luego paga una factura de \$578. ¿Cuánto dinero le queda?

**Solución:**  
$1250 + 345 = 1595$ (después del pago recibido)  
$1595 - 578 = 1017$  
Respuesta: \$1017.

### Problema 2 (Multiplicación aplicada)
Una fábrica produce 235 cajas con 24 botellas cada una. ¿Cuántas botellas produce en total?

**Solución:**  
$235 \times 24$  
Descomponemos: $235 \times (20+4) = 235\times20 + 235\times4 = 4700 + 940 = 5640$ botellas.

### Problema 3 (División con residuo)
Repartir 1000 caramelos entre 37 niños de manera equitativa. ¿Cuántos caramelos recibe cada uno y cuántos sobran?

**Solución:**  
Dividimos $1000 \div 37$  
$37 \times 27 = 999$ → cociente 27, residuo 1.  
Cada niño recibe 27 caramelos y sobra 1.

### Problema 4 (Propiedad distributiva)
Calcula $8 \times (125 + 37)$ mentalmente.

**Solución:**  
$8\times125 = 1000$, $8\times37=296$, suma $=1296$.

### Problema 5 (Jerarquía de operaciones)
Resuelve: $20 - 4 \times (3 + 2) + 16 \div 4$

**Solución paso a paso:**  
- Paréntesis: $3+2=5$  
- Multiplicación: $4\times5=20$  
- División: $16\div4=4$  
- Sustituimos: $20 - 20 + 4 = 4$  

Respuesta: $4$.

---

## 7. Ejercicios propuestos

1. Suma: $4897 + 2568 + 134$
2. Resta: $5000 - 2347$
3. Multiplica: $1234 \times 56$ (usa dos métodos)
4. Divide: $7890 \div 23$ (halla cociente y residuo)
5. Aplica jerarquía: $12 + 6 \times (8 - 3) - 15 \div 5$
6. Propiedad distributiva: $7 \times 999$ (sin calculadora, usa $999=1000-1$)
7. Un agricultor tiene 384 huevos y los empaca en docenas. ¿Cuántas docenas completas obtiene y cuántos huevos sueltos quedan?

*(Soluciones al final del documento)*

---

## 8. Errores comunes y consejos

- **Error en la resta con ceros**: Al pedir prestado a un cero, hay que convertir el cero en 10 después de pedir a la izquierda. Ejemplo: $500 - 1 = 499$ (no 500-1=400).
- **Olvidar llevar en suma**: Siempre verificar los acarreos.
- **Multiplicar sin desplazar**: En productos parciales, el primer producto parcial corresponde a las unidades, el segundo a las decenas (desplazado una posición), etc.
- **División incompleta**: Asegurarse de bajar todas las cifras del dividendo.
- **Confundir $a \div b$ con $b \div a$**: Leer bien el enunciado.

---

## 9. Aplicaciones en el mundo real

- **Finanzas**: Suma de ingresos, resta de gastos, multiplicación de cantidades por precio unitario, división de utilidades.
- **Ingeniería**: Cálculo de áreas (multiplicación), reparto de materiales (división), balances (sumas/restas).
- **Programación**: Todas las operaciones fundamentales son la base de algoritmos; la división entera (cociente y residuo) es clave en aritmética modular.

---

## Soluciones a los ejercicios propuestos

1. $4897+2568=7465$, $7465+134=7599$
2. $5000-2347=2653$ (puedes hacerlo con complemento: $5000-2000=3000$, luego $3000-347=2653$)
3. $1234\times50=61700$, $1234\times6=7404$, suma $=69104$
4. $7890 \div 23$: $23\times343=7889$, residuo $1$ → cociente $343$, residuo $1$
5. $8-3=5$, $6\times5=30$, $15\div5=3$, $12+30-3=39$
6. $7\times(1000-1)=7000-7=6993$
7. $384 \div 12 = 32$ docenas exactas, sobran $0$ huevos.

---

## Conclusión

Las cuatro operaciones fundamentales no son simples procedimientos mecánicos: constituyen el lenguaje básico de la aritmética y la base para temas posteriores como potenciación, radicación, razones, proporciones y teoría de números. Dominarlas con fluidez y comprensión permite abordar problemas más complejos con confianza.

En la próxima semana estudiaremos **Divisibilidad I**, donde aplicaremos la multiplicación y división para entender las relaciones entre números enteros.