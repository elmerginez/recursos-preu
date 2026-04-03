# 📚 Semana 02: Teoría de Conjuntos
**Área:** Ingenierías | **Ciclo:** Marzo - Julio 2026 CEPREUNA
**Materia:** Aritmética

---

## 1. Definición y Determinación de Conjuntos
[cite_start]Un conjunto es una colección de objetos llamados elementos. En el examen de admisión, se evalúa cómo se definen:

### A. Por Extensión (Forma Tabular)
[cite_start]Se nombran todos los elementos uno a uno.
* *Ejemplo:* $A = \{ \text{Lunes, Martes, Miércoles, Jueves, Viernes, Sábado, Domingo} \}$

### B. Por Comprensión (Forma Constructiva)
[cite_start]Se indica una propiedad común a todos los elementos mediante una ley de formación.
* **Estructura:** $\{ \text{Forma del elemento} \mid \text{Condición o Característica} \}$
* *Ejemplo (Nivel Ingenierías):* $B = \{ \frac{x+1}{2} \in \mathbb{Z} \mid x \in \mathbb{Z} \land 1 < x < 10 \}$
  *Para resolver esto, primero hallas los valores de $x$ ($2,3,4...9$), luego aplicas la fórmula $\frac{x+1}{2}$ y solo te quedas con los resultados que sean enteros.*

---

## [cite_start]2. Relaciones entre Conjuntos 

### 2.1 Pertenencia ($\in$)
[cite_start]Relaciona un **elemento** con un **conjunto**.
> **Regla de Oro:** El elemento debe estar escrito **exactamente igual** a como aparece dentro del conjunto.
* Sea $M = \{2, \{5\}, 8, \emptyset\}$.
  * $2 \in M$ (Verdadero)
  * $5 \in M$ (Falso, el elemento es $\{5\}$)
  * $\{5\} \in M$ (Verdadero)
  * $\emptyset \in M$ (Verdadero, porque está en la lista)

### 2.2 Inclusión ($\subset$)
[cite_start]Relaciona un **conjunto** con otro **conjunto**. [cite_start]Se dice que $A \subset B$ si todos los elementos de $A$ están en $B$.
* **Subconjuntos de A:** Si $n(A) = k$, el número de subconjuntos es $2^k$.
* **Subconjuntos Propios:** Son todos excepto el mismo conjunto: $2^k - 1$.

---

## [cite_start]3. Conjuntos Especiales 
1. [cite_start]**Vacío ($\emptyset$ o $\{ \}$):** Carece de elementos. **Ojo:** El vacío está incluido en TODOS los conjuntos.
2. [cite_start]**Unitario (Singletón):** Tiene un solo elemento.
   * *Pregunta Clásica:* Si $A = \{a+8, 2a-4, 20\}$ es unitario, halla $a$. 
     *(Solución: $a+8=20 \Rightarrow a=12$. Comprobamos: $2(12)-4=20$. ¡Correcto!)*
3. **Universal ($U$):** Conjunto referencial que contiene a todos los demás.
4. **Potencia ($P(A)$):** Es el conjunto formado por todos los subconjuntos de $A$.

---

## [cite_start]4. Operaciones entre Conjuntos 

| Operación | Símbolo | Definición Lógica | Interpretación |
| :--- | :---: | :--- | :--- |
| **Unión** | $\cup$ | $x \in A \lor x \in B$ | Elementos de A, de B o de ambos. |
| **Intersección** | $\cap$ | $x \in A \land x \in B$ | Solo elementos comunes. |
| **Diferencia** | $-$ | $x \in A \land x \notin B$ | Elementos que están SOLO en A. |
| **Dif. Simétrica** | $\Delta$ | $(A \cup B) - (A \cap B)$ | Elementos de A o B, pero no de ambos. |
| **Complemento** | $A^c$ | $x \in U \land x \notin A$ | Lo que le falta a A para ser el Universo. |



[Image of Venn diagrams showing union, intersection, difference, and symmetric difference]


---

## [cite_start]5. Leyes del Álgebra de Conjuntos 
Estas leyes permiten simplificar expresiones complejas, igual que en Lógica:

1. **Idempotencia:** $A \cup A = A$ ; $A \cap A = A$
2. **Conmutativa:** $A \cup B = B \cup A$
3. **Leyes de Morgan:** * $(A \cup B)^c = A^c \cap B^c$
   * $(A \cap B)^c = A^c \cup B^c$
4. **Leyes de Absorción (Vital para exámenes):**
   * $A \cup (A \cap B) = A$
   * $A \cap (A \cup B) = A$
   * $A \cup (A^c \cap B) = A \cup B$

---

## [cite_start]6. Cuantificadores 
* **Universal ($\forall$):** "Para todo". [cite_start]Se cumple para todos los elementos del conjunto.
* **Existencial ($\exists$):** "Existe al menos uno". [cite_start]Se cumple si al menos un elemento satisface la condición.

---

## 📝 Ejercicios Resueltos (Nivel CEPREUNA)

### Problema 1: Cardinalidad
De un grupo de 80 postulantes a Ingeniería:
- 40 postulan a Ingeniería Civil.
- 30 postulan a Ingeniería de Sistemas.
- 15 postulan a ambas carreras.
**¿Cuántos no postulan a ninguna de estas dos?**

**Solución:**
Usamos el Diagrama de Venn:
1. Intersección (Ambas): $15$.
2. Solo Civil: $40 - 15 = 25$.
3. Solo Sistemas: $30 - 15 = 15$.
4. Total que postulan: $25 + 15 + 15 = 55$.
5. No postulan a ninguna: $80 - 55 = 25$.
**Respuesta:** 25 alumnos.



### Problema 2: Conjunto Potencia
Si el conjunto $A$ tiene 5 elementos, ¿cuántos subconjuntos propios tiene?
**Solución:**
Fórmula: $2^{n(A)} - 1$
$2^5 - 1 = 32 - 1 = 31$.
**Respuesta:** 31 subconjuntos propios.

---

<div style="background: rgba(255, 165, 0, 0.1); border-left: 5px solid #ffa500; padding: 15px; margin: 20px 0;">
  <strong>⚠️ ¡Error Común!</strong> Confundir $\in$ con $\subset$. Recuerda: para que algo sea inclusión ($\subset$), debe tener llaves que envuelvan a un elemento que ya pertenece al conjunto.
</div>