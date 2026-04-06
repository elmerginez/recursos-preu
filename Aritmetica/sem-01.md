# Semana 1: Lógica Proposicional

## 1. Introducción a la lógica proposicional

La lógica proposicional es la rama de la lógica que estudia las **proposiciones** (enunciados que pueden ser verdaderos o falsos) y las relaciones que se establecen entre ellas mediante conectores lógicos. Es fundamental para el razonamiento matemático, la computación y la ingeniería de circuitos.

### 1.1 Proposiciones simples y compuestas

- **Proposición simple**: Es aquella que no contiene conectores lógicos. Expresa una afirmación única que puede ser verdadera (V) o falsa (F), pero no ambas.
  - Ejemplos:
    - "5 es un número primo" (V)
    - "La Luna es de queso" (F)
    - "x + 3 = 7" (No es proposición porque depende del valor de x, a menos que se cuantifique)

- **Proposición compuesta**: Se forma combinando dos o más proposiciones simples mediante conectores lógicos (conjunciones, disyunciones, negaciones, etc.).
  - Ejemplo: "5 es primo **y** 2 + 2 = 4"

### 1.2 Variables proposicionales

Usamos letras minúsculas como \( p, q, r, \dots \) para representar proposiciones. A cada variable se le asigna un valor de verdad: **V** (1) o **F** (0).

## 2. Conectores lógicos (funciones veritativas)

Los conectores lógicos son operadores que permiten construir proposiciones compuestas. Su significado se define mediante **tablas de verdad**.

### 2.1 Negación (\(\neg\))

Invierte el valor de verdad de una proposición.

| \(p\) | \(\neg p\) |
|:---:|:---:|
| V   | F   |
| F   | V   |

- **Ejemplo**:  
  \(p\): "Está lloviendo"  
  \(\neg p\): "No está lloviendo"

### 2.2 Conjunción (\(\land\))

Verdadera solo si **ambas** proposiciones son verdaderas.

| \(p\) | \(q\) | \(p \land q\) |
|:---:|:---:|:---:|
| V   | V   | V   |
| V   | F   | F   |
| F   | V   | F   |
| F   | F   | F   |

- **Ejemplo**:  
  \(p\): "El semáforo está en verde"  
  \(q\): "El coche puede pasar"  
  \(p \land q\): "El semáforo está en verde **y** el coche puede pasar"

### 2.3 Disyunción inclusiva (\(\lor\))

Verdadera si **al menos una** de las proposiciones es verdadera.

| \(p\) | \(q\) | \(p \lor q\) |
|:---:|:---:|:---:|
| V   | V   | V   |
| V   | F   | V   |
| F   | V   | V   |
| F   | F   | F   |

- **Ejemplo**:  
  \(p\): "Apruebo el examen"  
  \(q\): "Recupero con trabajo práctico"  
  \(p \lor q\): "Apruebo el examen **o** recupero con trabajo práctico" (pueden darse ambas).

### 2.4 Disyunción exclusiva (\(\oplus\) o \(\veebar\))

Verdadera si **exactamente una** de las proposiciones es verdadera.

| \(p\) | \(q\) | \(p \oplus q\) |
|:---:|:---:|:---:|
| V   | V   | F   |
| V   | F   | V   |
| F   | V   | V   |
| F   | F   | F   |

- **Ejemplo**:  
  "Hoy es martes **o** hoy es miércoles" (no pueden ser ambos).

### 2.5 Implicación (\(\rightarrow\))

\(p \rightarrow q\) se lee "si \(p\) entonces \(q\)". Es falsa solo cuando \(p\) es verdadera y \(q\) es falsa. En los demás casos es verdadera.

| \(p\) | \(q\) | \(p \rightarrow q\) |
|:---:|:---:|:---:|
| V   | V   | V   |
| V   | F   | F   |
| F   | V   | V   |
| F   | F   | V   |

- **Ejemplo**:  
  \(p\): "Estudio lógica"  
  \(q\): "Aprendo"  
  \(p \rightarrow q\): "Si estudio lógica, entonces aprendo"

### 2.6 Bicondicional (\(\leftrightarrow\))

\(p \leftrightarrow q\) se lee "\(p\) si y solo si \(q\)". Es verdadera cuando ambas tienen el mismo valor de verdad.

| \(p\) | \(q\) | \(p \leftrightarrow q\) |
|:---:|:---:|:---:|
| V   | V   | V   |
| V   | F   | F   |
| F   | V   | F   |
| F   | F   | V   |

- **Ejemplo**:  
  \(p\): "El triángulo tiene tres lados iguales"  
  \(q\): "El triángulo es equilátero"  
  \(p \leftrightarrow q\): "El triángulo tiene tres lados iguales **si y solo si** es equilátero"

## 3. Tablas de verdad para expresiones complejas

Para evaluar proposiciones compuestas con varias variables, construimos tablas de verdad considerando todas las combinaciones posibles de valores de verdad.

### Ejemplo paso a paso

Construir la tabla de verdad de \((p \land q) \rightarrow \neg r\)

**Paso 1**: Identificar variables: \(p, q, r\) → \(2^3 = 8\) filas.

**Paso 2**: Calcular subexpresiones.

| \(p\) | \(q\) | \(r\) | \(p \land q\) | \(\neg r\) | \((p \land q) \rightarrow \neg r\) |
|:---:|:---:|:---:|:---:|:---:|:---:|
| V   | V   | V   | V   | F   | F   |
| V   | V   | F   | V   | V   | V   |
| V   | F   | V   | F   | F   | V   |
| V   | F   | F   | F   | V   | V   |
| F   | V   | V   | F   | F   | V   |
| F   | V   | F   | F   | V   | V   |
| F   | F   | V   | F   | F   | V   |
| F   | F   | F   | F   | V   | V   |

### Ejercicio para el estudiante

Construye la tabla de verdad de \((p \rightarrow q) \leftrightarrow (\neg p \lor q)\) ¿Qué observas?

## 4. Implicación lógica y equivalencias lógicas

### 4.1 Implicación lógica

Decimos que una fórmula \(A\) **implica lógicamente** a \(B\) (denotado \(A \Rightarrow B\)) si en todas las filas de la tabla de verdad donde \(A\) es verdadera, \(B\) también lo es. Es decir, \(A \rightarrow B\) es una tautología.

- **Ejemplo**: \(p \land q \Rightarrow p\)  
  Siempre que \(p \land q\) es V, \(p\) es V.

### 4.2 Equivalencia lógica

Dos fórmulas \(A\) y \(B\) son **lógicamente equivalentes** (\(A \equiv B\)) si tienen exactamente los mismos valores de verdad para todas las combinaciones de sus variables. Es decir, \(A \leftrightarrow B\) es una tautología.

- **Ejemplo**: \(p \rightarrow q \equiv \neg p \lor q\)  
  Compruébalo con una tabla de verdad.

## 5. Equivalencias notables (Leyes del álgebra proposicional)

Son identidades que permiten simplificar y transformar expresiones lógicas.

| Nombre | Equivalencia |
|--------|---------------|
| **Doble negación** | \(\neg (\neg p) \equiv p\) |
| **Idempotencia** | \(p \land p \equiv p\), \(p \lor p \equiv p\) |
| **Conmutatividad** | \(p \land q \equiv q \land p\), \(p \lor q \equiv q \lor p\) |
| **Asociatividad** | \((p \land q) \land r \equiv p \land (q \land r)\), análogo para \(\lor\) |
| **Distributividad** | \(p \land (q \lor r) \equiv (p \land q) \lor (p \land r)\) <br> \(p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)\) |
| **De Morgan** | \(\neg (p \land q) \equiv \neg p \lor \neg q\) <br> \(\neg (p \lor q) \equiv \neg p \land \neg q\) |
| **Implicación** | \(p \rightarrow q \equiv \neg p \lor q\) |
| **Contrarrecíproco** | \(p \rightarrow q \equiv \neg q \rightarrow \neg p\) |
| **Bicondicional** | \(p \leftrightarrow q \equiv (p \rightarrow q) \land (q \rightarrow p)\) <br> \(p \leftrightarrow q \equiv (p \land q) \lor (\neg p \land \neg q)\) |
| **Absorción** | \(p \land (p \lor q) \equiv p\) <br> \(p \lor (p \land q) \equiv p\) |
| **Identidad** | \(p \land V \equiv p\), \(p \lor F \equiv p\) |
| **Dominación** | \(p \lor V \equiv V\), \(p \land F \equiv F\) |
| **Complemento** | \(p \land \neg p \equiv F\), \(p \lor \neg p \equiv V\) |

### Ejemplo de simplificación

Simplificar \((p \rightarrow q) \land (\neg p \rightarrow q)\):

\[
\begin{align*}
(p \rightarrow q) \land (\neg p \rightarrow q) &\equiv (\neg p \lor q) \land (\neg \neg p \lor q) \quad \text{(Implicación)}\\
&\equiv (\neg p \lor q) \land (p \lor q) \quad \text{(Doble negación)}\\
&\equiv (\neg p \land p) \lor q \quad \text{(Distributividad: } (A \lor q) \land (B \lor q) \equiv (A \land B) \lor q\text{)}\\
&\equiv F \lor q \equiv q
\end{align*}
\]

Resultado: la expresión equivale simplemente a \(q\).

## 6. Circuitos lógicos

Los circuitos lógicos (o de conmutación) son representaciones físicas o esquemáticas de expresiones proposicionales. Se usan en electrónica digital y computadoras.

### 6.1 Componentes básicos (interruptores)

Modelamos proposiciones como interruptores que pueden estar **cerrados** (verdadero, paso de corriente) o **abiertos** (falso, no pasa corriente). Las combinaciones serie/paralelo corresponden a conectores:

- **Circuito en serie**: Dos interruptores \(p\) y \(q\) en serie → la corriente pasa solo si ambos están cerrados. Equivale a \(p \land q\).

- **Circuito en paralelo**: Dos interruptores en paralelo → la corriente pasa si al menos uno está cerrado. Equivale a \(p \lor q\).

- **Circuito con inversor (negación)**: Un interruptor normalmente cerrado que se abre cuando la proposición es verdadera, o viceversa. Se representa con una compuerta NOT.

### 6.2 Compuertas lógicas (para diseño digital)

| Compuerta | Símbolo | Expresión |
|-----------|---------|-----------|
| AND       | &       | \(A \cdot B\) o \(A \land B\) |
| OR        | ≥1      | \(A + B\) o \(A \lor B\) |
| NOT       | ○       | \(\overline{A}\) o \(\neg A\) |
| NAND      |         | \(\overline{A \land B}\) |
| NOR       |         | \(\overline{A \lor B}\) |
| XOR       | =1      | \(A \oplus B\) |

### 6.3 De la expresión al circuito

Construir el circuito lógico para \((p \land q) \lor (\neg p \land r)\)

**Pasos**:
1. Identificar subexpresiones: \(p \land q\) (AND), \(\neg p\) (NOT), luego \(\neg p \land r\) (AND).
2. Combinar los dos resultados con una OR.

**Diagrama textual**:
p ----| |
| AND |----
q ----||
OR ---- salida
p ----|NOT|----| |
|____| | AND |----/
r ------------||


### 6.4 Simplificación de circuitos usando álgebra proposicional

Un circuito puede reducirse a otro equivalente más simple usando las leyes lógicas. Por ejemplo, el circuito \((p \land q) \lor (p \land \neg q)\) se simplifica a \(p\) por la ley de distribución y complemento:

\[
(p \land q) \lor (p \land \neg q) \equiv p \land (q \lor \neg q) \equiv p \land V \equiv p
\]

## 7. Problemas resueltos

### Problema 1 (Básico)

Determina el valor de verdad de la siguiente proposición compuesta, sabiendo que \(p\) es verdadera, \(q\) falsa y \(r\) verdadera:  
\((p \rightarrow \neg q) \leftrightarrow (r \land \neg p)\)

**Solución**:  
- \(p = V\), \(q = F\), \(r = V\)  
- \(\neg q = V\)  
- \(p \rightarrow \neg q = V \rightarrow V = V\)  
- \(\neg p = F\)  
- \(r \land \neg p = V \land F = F\)  
- \(V \leftrightarrow F = F\)  
Resultado: **Falso**.

### Problema 2 (Intermedio)

Demostrar que \((p \rightarrow q) \land (p \rightarrow \neg q) \equiv \neg p\) usando leyes lógicas.

**Solución**:

\[
\begin{align*}
(p \rightarrow q) \land (p \rightarrow \neg q) &\equiv (\neg p \lor q) \land (\neg p \lor \neg q) \quad \text{(Implicación)}\\
&\equiv \neg p \lor (q \land \neg q) \quad \text{(Distributividad)}\\
&\equiv \neg p \lor F \equiv \neg p
\end{align*}
\]

### Problema 3 (Avanzado - Circuito)

Diseña un circuito para la función lógica de tres entradas \(a, b, c\) que sea verdadera solo cuando exactamente una de las tres entradas sea verdadera. Simplifica la expresión.

**Solución**:

La condición "exactamente una verdadera" se expresa como:

\[
(a \land \neg b \land \neg c) \lor (\neg a \land b \land \neg c) \lor (\neg a \land \neg b \land c)
\]

Esta expresión no se simplifica a algo más corto que tres términos AND con tres literales cada uno. El circuito requerirá tres compuertas AND de tres entradas (o combinación de AND de dos entradas) y una OR de tres entradas.

## 8. Ejercicios propuestos

1. **Tablas de verdad**: Construye la tabla de verdad de \((p \lor \neg q) \rightarrow (r \land \neg p)\)
2. **Equivalencia**: Demuestra usando leyes que \((p \rightarrow q) \land (q \rightarrow r) \rightarrow (p \rightarrow r)\) es una tautología.
3. **Simplificación**: Simplifica al máximo: \((p \land q) \lor (\neg p \land q) \lor (p \land \neg q)\)
4. **Circuito**: Dibuja el circuito lógico (compuertas) para la expresión \(\overline{(p \land q) \lor r}\) y luego escríbelo usando solo compuertas NAND.
5. **Traducción**: Escribe en lenguaje lógico: "Si estudio y practico, entonces apruebo; pero si no practico, entonces no apruebo".

## 9. Respuestas breves a los ejercicios

1. Tabla de verdad (8 filas). Última columna: F, V, V, V, V, V, V, V (depende del orden).
2. Simplificar a \(V\) aplicando implicación, distributiva y complemento.
3. \(q \lor p\) (equivalente a \(p \lor q\))
4. \(\overline{(p \land q) \lor r} = \overline{p \land q} \land \overline{r}\) (De Morgan). Usando NAND: \(\overline{p \land q} = p \uparrow q\); luego \((p \uparrow q) \land \overline{r}\) requiere una NAND adicional.
5. \((E \land P) \rightarrow A\) y \((\neg P) \rightarrow \neg A\). Equivalentemente \((E \land P) \rightarrow A\) y \(A \rightarrow P\) (contrapositiva). Se puede unir.

---

**Fin de la semana 1 - Lógica Proposicional**