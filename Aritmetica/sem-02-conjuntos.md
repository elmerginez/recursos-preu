# Semana 2: Teoría de Conjuntos

## 1. Determinación de un conjunto

Un **conjunto** es una colección bien definida de objetos distintos, llamados **elementos**. Se denota usualmente con letras mayúsculas: $A, B, C, \dots$ y los elementos se escriben entre llaves $\{ \}$.

### 1.1. Formas de determinar un conjunto

#### Por extensión (o tabulación)
Se listan explícitamente todos los elementos entre llaves, separados por comas.

**Ejemplo:**  
$$A = \{2, 4, 6, 8, 10\}$$  
$$B = \{\text{rojo}, \text{verde}, \text{azul}\}$$

#### Por comprensión (o por descripción)
Se define mediante una propiedad que cumplen todos sus elementos y solo ellos. Se usa la notación $\{x \mid P(x)\}$ o $\{x : P(x)\}$.

**Ejemplo:**  
$$C = \{x \in \mathbb{N} \mid x \text{ es par y } x \leq 10\} = \{2,4,6,8,10\}$$  
$$D = \{x \mid x \text{ es un color primario}\} = \{\text{rojo}, \text{verde}, \text{azul}\}$$

> **Nivel básico:** Para entender la diferencia, piensa que “por extensión” es hacer una lista, y “por comprensión” es dar la regla que cumplen los elementos.

> **Nivel intermedio:** A veces un mismo conjunto puede definirse de ambas maneras. La elección depende de si el conjunto es finito y manejable o infinito.

> **Nivel avanzado:** En teoría de conjuntos axiomática, la comprensión irrestricta lleva a paradojas (como la de Russell). Por ello se usa el esquema de comprensión restringida.

---

## 2. Relaciones entre conjuntos

### 2.1. Pertenencia e inclusión

- **Pertenencia ($\in$):** Indica que un objeto es elemento de un conjunto.  
  $a \in A$ significa “$a$ pertenece a $A$”.  
  $a \notin A$ significa “$a$ no pertenece a $A$”.

- **Inclusión ($\subseteq$):** $A \subseteq B$ si todo elemento de $A$ es también elemento de $B$. Se dice “$A$ es subconjunto de $B$”.

- **Igualdad ($=$):** $A = B$ si $A \subseteq B$ y $B \subseteq A$.

- **Subconjunto propio ($\subset$):** $A \subset B$ si $A \subseteq B$ y $A \neq B$. Algunos autores usan $\subsetneq$ para evitar ambigüedad.

**Ejemplos:**  
$\{1,3\} \subseteq \{1,2,3,4\}$  
$\{1,2\} \not\subseteq \{2,3,4\}$ porque $1 \notin \{2,3,4\}$  
$\{a,b,c\} = \{c,b,a\}$ (el orden no importa)

### 2.2. Conjuntos especiales

- **Conjunto vacío ($\emptyset$ o $\{\}$):** No tiene elementos. Es subconjunto de todo conjunto: $\emptyset \subseteq A$ para cualquier $A$.

- **Conjunto universal ($U$):** En un contexto dado, contiene todos los elementos bajo consideración. No es único absoluto; depende del problema.

**Ejemplo:** En problemas de números enteros, $U = \mathbb{Z}$. En estadística descriptiva, $U$ podría ser la población total.

> **Nivel avanzado:** En teoría axiomática de conjuntos (ZF) no existe un conjunto universal, pues llevaría a paradojas. Se trabaja con universos relativos.

---

## 3. Operaciones entre conjuntos

Sean $A$ y $B$ subconjuntos de un universo $U$.

| Operación        | Notación     | Definición                                   | Ejemplo ($U = \{1,2,3,4,5\}$, $A=\{1,2,3\}$, $B=\{3,4,5\}$) |
|-----------------|--------------|----------------------------------------------|------------------------------------------------------------|
| **Unión**       | $A \cup B$   | $\{x \mid x \in A \text{ o } x \in B\}$      | $\{1,2,3,4,5\}$                                            |
| **Intersección**| $A \cap B$   | $\{x \mid x \in A \text{ y } x \in B\}$      | $\{3\}$                                                    |
| **Diferencia**  | $A \setminus B$ (o $A-B$) | $\{x \mid x \in A \text{ y } x \notin B\}$ | $\{1,2\}$                                                  |
| **Complemento** | $A^c$ (o $\overline{A}$, $A'$) | $\{x \in U \mid x \notin A\}$               | $\{4,5\}$                                                  |
| **Diferencia simétrica** | $A \triangle B$ | $(A \setminus B) \cup (B \setminus A)$      | $\{1,2,4,5\}$                                              |

**Diagramas de Venn** son una herramienta visual muy útil para entender estas operaciones.

> **Ejemplo básico:** Si $A = \{perros\}$ y $B = \{mamíferos\}$, entonces $A \cap B = \{perros\}$, $A \cup B = \{mamíferos\}$, $A \setminus B = \emptyset$ (si todo perro es mamífero).

> **Ejemplo intermedio:** Demuestra que $A \triangle B = (A \cup B) \setminus (A \cap B)$. Verifica con números: $A=\{1,2,3\}, B=\{3,4,5\}$, entonces $(A \cup B)=\{1,2,3,4,5\}$, $(A \cap B)=\{3\}$, su diferencia es $\{1,2,4,5\}$, igual que $A \triangle B$.

> **Ejemplo avanzado:** Propiedades de la diferencia simétrica: es conmutativa, asociativa, y cumple $A \triangle \emptyset = A$, $A \triangle A = \emptyset$, y $A \triangle B = (A^c \triangle B^c)$.

---

## 4. Conjuntos especiales

### 4.1. Conjunto potencia o de partes

El **conjunto potencia** de $A$, denotado $\mathcal{P}(A)$ o $2^A$, es el conjunto de todos los subconjuntos de $A$ (incluyendo el vacío y el propio $A$).

- Si $|A| = n$ (número de elementos), entonces $|\mathcal{P}(A)| = 2^n$.

**Ejemplo:** $A = \{a,b\}$  
$\mathcal{P}(A) = \{\emptyset, \{a\}, \{b\}, \{a,b\}\}$ (4 elementos)

### 4.2. Conjuntos disjuntos

Dos conjuntos $A$ y $B$ son **disjuntos** si $A \cap B = \emptyset$.

### 4.3. Partición de un conjunto

Una **partición** de un conjunto $X$ es una colección de subconjuntos no vacíos de $X$, disjuntos dos a dos, cuya unión es $X$. Es decir, dividen a $X$ en partes que no se solapan y lo cubren completamente.

**Ejemplo:** $\{\{1,2\}, \{3,5\}, \{4\}\}$ es una partición de $\{1,2,3,4,5\}$.

> **Aplicación:** Las clases de equivalencia de una relación de equivalencia forman una partición.

---

## 5. Leyes del Álgebra de Conjuntos

Estas leyes son análogas a las del álgebra booleana y permiten simplificar expresiones conjuntistas.

Sean $A, B, C$ subconjuntos de un universo $U$.

| **Ley**                | **Expresión**                                   |
|------------------------|-------------------------------------------------|
| **Idempotencia**       | $A \cup A = A$,  $A \cap A = A$                |
| **Conmutativa**        | $A \cup B = B \cup A$,  $A \cap B = B \cap A$ |
| **Asociativa**         | $(A \cup B) \cup C = A \cup (B \cup C)$, análogo para intersección |
| **Distributiva**       | $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$ <br> $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$ |
| **Identidad**          | $A \cup \emptyset = A$,  $A \cap U = A$       |
| **Complemento**        | $A \cup A^c = U$,  $A \cap A^c = \emptyset$   |
| **Doble complemento**  | $(A^c)^c = A$                                 |
| **Leyes de De Morgan** | $(A \cup B)^c = A^c \cap B^c$ <br> $(A \cap B)^c = A^c \cup B^c$ |
| **Absorción**          | $A \cup (A \cap B) = A$,  $A \cap (A \cup B) = A$ |

### Ejemplos de aplicación

**Ejemplo básico:** Simplifica $(A \cap B) \cup (A \cap B^c)$.  
Por la ley distributiva: $A \cap (B \cup B^c) = A \cap U = A$.

**Ejemplo intermedio:** Demuestra que $A \setminus (B \cup C) = (A \setminus B) \cap (A \setminus C)$.  
Usando definiciones:  
$x \in A \setminus (B \cup C) \iff x \in A \land x \notin (B \cup C) \iff x \in A \land (x \notin B \land x \notin C) \iff (x \in A \land x \notin B) \land (x \in A \land x \notin C) \iff x \in (A \setminus B) \cap (A \setminus C)$.

**Ejemplo avanzado:** Verifica la ley de De Morgan para tres conjuntos: $(A \cup B \cup C)^c = A^c \cap B^c \cap C^c$. Se puede demostrar por inducción o aplicando dos veces la ley binaria.

---

## 6. Cuantificadores

En teoría de conjuntos usamos cuantificadores para expresar proposiciones sobre elementos.

### 6.1. Cuantificador universal ($\forall$)
Significa “para todo” o “para cada”.  
$\forall x \in A, P(x)$ se lee: “Para todo $x$ perteneciente a $A$, se cumple $P(x)$”.

**Ejemplo:** $\forall x \in \mathbb{N}, x+1 > x$ (verdadero).

### 6.2. Cuantificador existencial ($\exists$)
Significa “existe al menos un”.  
$\exists x \in A : P(x)$ se lee: “Existe un $x$ en $A$ tal que $P(x)$”.

**Ejemplo:** $\exists x \in \mathbb{Z} : x^2 = 4$ (verdadero, $x=2$ o $x=-2$).

### 6.3. Negación de cuantificadores

- $\neg (\forall x \in A, P(x)) \equiv \exists x \in A : \neg P(x)$  
- $\neg (\exists x \in A : P(x)) \equiv \forall x \in A, \neg P(x)$

**Ejemplo:** Negar “Todos los números primos son impares”.  
La negación es “Existe un número primo que es par” (el 2).

### 6.4. Aplicación en conjuntos

La definición de subconjunto usa cuantificador universal:  
$A \subseteq B \iff \forall x (x \in A \rightarrow x \in B)$.

La definición de unión:  
$x \in A \cup B \iff (x \in A) \lor (x \in B)$.

**Ejemplo de demostración con cuantificadores:**  
Prueba que $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$.  
Demostramos doble inclusión:  
- $\forall x [x \in A \cap (B \cup C) \rightarrow x \in (A \cap B) \cup (A \cap C)]$  
- $\forall x [x \in (A \cap B) \cup (A \cap C) \rightarrow x \in A \cap (B \cup C)]$  
Cada paso usa definiciones y lógica proposicional con cuantificadores.

> **Nivel avanzado:** En lógica de predicados, los cuantificadores permiten formalizar completamente la teoría de conjuntos. Por ejemplo, el axioma de extensionalidad: $\forall A \forall B (\forall x (x \in A \leftrightarrow x \in B) \rightarrow A = B)$.

---

## Ejercicios propuestos (con soluciones)

1. **Básico:** Dados $U = \{1,2,3,4,5,6\}$, $A=\{1,2,3\}$, $B=\{3,4,5\}$, calcula:  
   $A \cup B$, $A \cap B$, $A \setminus B$, $B \setminus A$, $A^c$, $(A \cup B)^c$.

   **Solución:**  
   $A \cup B = \{1,2,3,4,5\}$  
   $A \cap B = \{3\}$  
   $A \setminus B = \{1,2\}$  
   $B \setminus A = \{4,5\}$  
   $A^c = \{4,5,6\}$  
   $(A \cup B)^c = \{6\}$

2. **Intermedio:** Demuestra usando las leyes del álgebra de conjuntos que  
   $A \cup (B \cap A^c) = A \cup B$.

   **Solución:**  
   $A \cup (B \cap A^c) = (A \cup B) \cap (A \cup A^c)$ (distributiva)  
   $= (A \cup B) \cap U = A \cup B$.

3. **Avanzado:** Dados $A$ y $B$ subconjuntos de $U$, prueba que $A \triangle B = \emptyset$ si y solo si $A = B$.

   **Solución:**  
   ($\Rightarrow$) Si $A \triangle B = \emptyset$, entonces ningún elemento está en $A \setminus B$ ni en $B \setminus A$, luego $A \subseteq B$ y $B \subseteq A$, así $A=B$.  
   ($\Leftarrow$) Si $A=B$, entonces $A \setminus B = \emptyset$ y $B \setminus A = \emptyset$, por tanto $A \triangle B = \emptyset$.

---

## Resumen

- Un conjunto se define por extensión (lista) o comprensión (propiedad).
- Relaciones: pertenencia ($\in$), inclusión ($\subseteq$), igualdad.
- Operaciones: unión, intersección, diferencia, complemento, diferencia simétrica.
- Conjuntos especiales: vacío, universal, potencia, particiones.
- Leyes del álgebra de conjuntos (análogas a la lógica proposicional).
- Cuantificadores: universal ($\forall$) y existencial ($\exists$), con sus negaciones.

Este material cubre desde los fundamentos hasta aplicaciones avanzadas, preparando para temas posteriores como probabilidad, relaciones y funciones.