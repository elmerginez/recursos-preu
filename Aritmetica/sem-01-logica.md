# 🏛️ Semana 01: Lógica Proposicional (Teoría y Práctica)
**Área:** Ingenierías | **Ciclo:** Marzo - Julio 2026 CEPREUNA
**Materia:** Aritmética

---

## Teoría Normal en Markdown
La lógica proposicional es fundamental para el examen.

<div style="background-color: rgba(255, 0, 0, 0.1); border-left: 4px solid red; padding: 15px; border-radius: 5px; margin: 20px 0;">
  <h3 style="color: #ff6b6b; margin-top: 0;">🚨 ¡Ojo al dato!</h3>
  <p>En las preguntas tipo <b>DECO</b> de la UNAP, la palabra "pero" equivale a una conjunción $\land$.</p>
</div>

<div align="center">
  <span style="color: #4ade80; font-size: 1.2rem; font-weight: bold;">
    ¡Ese truco vale oro en el simulacro!
  </span>
</div>

## 1. Enunciados y Proposiciones
[cite_start]Antes de operar, debemos saber qué es válido en la lógica y qué no.

### A. Enunciado
Es cualquier frase, oración o expresión matemática. 
* *Ejemplo:* "¡Qué frío hace en Juliaca!", "$x + 2 = 5$", "¿Qué hora es?".

### B. Proposición Lógica ($p, q, r, \dots$)
[cite_start]Es un enunciado aseverativo (afirma o niega algo) que tiene la propiedad exclusiva de ser **Verdadero (V)** o **Falso (F)**, pero nunca ambos a la vez.
* **Sí son proposiciones:**
  * "El lago Titicaca es el más alto del mundo." (V)
  * "$2 + 2 = 5$" (F)
* **No son proposiciones:**
  * Preguntas, exclamaciones, deseos, órdenes ("¡Ingresaré a la UNAP!").
  * **Enunciados abiertos:** "$x + 3 = 8$" (No sabemos si es V o F porque no conocemos el valor de $x$. Si le damos un valor, se convierte en proposición).

---

## [cite_start]2. Conectivos Lógicos y Funciones Veritativas 
Son los símbolos que enlazan proposiciones simples para formar compuestas. Cada conectivo tiene palabras equivalentes en nuestro idioma.

### 2.1 Conjunción ($\land$)
* **Se lee:** "p y q", "p pero q", "p sin embargo q", "p además q".
* **Regla:** Solo es Verdadera ($V$) cuando **ambas** proposiciones son Verdaderas.

### 2.2 Disyunción Débil o Inclusiva ($\lor$)
* **Se lee:** "p o q", "p a menos que q".
* **Regla:** Solo es Falsa ($F$) cuando **ambas** proposiciones son Falsas. (Admite que ambas pasen a la vez).

### 2.3 Disyunción Fuerte o Exclusiva ($\Delta$)
* **Se lee:** "O bien p o bien q" (pero no ambas).
* **Regla:** Es Verdadera ($V$) solo cuando los valores son **diferentes**.

### 2.4 Condicional ($\to$)
* **Se lee:** "Si p entonces q", "p implica q", "q porque p" (¡Ojo! El orden importa: $p$ es la causa/antecedente y $q$ el efecto/consecuente).
* **Regla:** Solo es Falsa ($F$) cuando partimos de una verdad y llegamos a una falsedad ($V \to F = F$).

### 2.5 Bicondicional ($\leftrightarrow$)
* **Se lee:** "p si y solo si q", "p es condición necesaria y suficiente para q".
* **Regla:** Es Verdadera ($V$) solo cuando **ambos valores son iguales**.



---

## [cite_start]3. Tablas de Verdad y Evaluación de Esquemas 

Para evaluar una fórmula compleja, seguimos una jerarquía:
1. Paréntesis y corchetes.
2. Negación ($\sim$).
3. Conjunción ($\land$) y Disyunción ($\lor$).
4. Condicional ($\to$).
5. Bicondicional ($\leftrightarrow$) y Disyunción Fuerte ($\Delta$).

### 📝 Caso Práctico Resuelto: Evaluación
**Problema:** Evaluar el esquema molecular: $(p \lor \sim q) \to (p \land q)$ e indicar si es Tautología, Contradicción o Contingencia.

**Solución Paso a Paso:**
Como hay 2 variables ($p, q$), la tabla tendrá $2^2 = 4$ filas.

| $p$ | $q$ | $(p$ | $\lor$ | $\sim q)$ | $\to$ | $(p$ | $\land$ | $q)$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| V | V | V | **V** | F | **V** | V | **V** | V |
| V | F | V | **V** | V | **F** | V | **F** | F |
| F | V | F | **F** | F | **V** | F | **F** | V |
| F | F | F | **V** | V | **F** | F | **F** | F |
| | | 1 | **3** | 2 | **Rpta** | 1 | **2** | 1 |

* **Análisis:** La columna principal (debajo de $\to$) tiene valores V y F.
* **Respuesta:** El esquema es una **Contingencia**.

---

## [cite_start]4. Implicación y Equivalencia Lógica 

* **Implicación Lógica ($\Rightarrow$):** Decimos que $A \Rightarrow B$ si y solo si al hacer la tabla de verdad de $A \to B$, el resultado es una Tautología absoluta.
* **Equivalencia Lógica ($\equiv$):** Decimos que $A \equiv B$ si y solo si la tabla de verdad de $A \leftrightarrow B$ es una Tautología. [cite_start]Significa que ambas fórmulas valen exactamente lo mismo y pueden reemplazarse entre sí.

---

## [cite_start]5. Leyes del Álgebra Proposicional (Equivalencias Notables) 
Estas leyes te salvan la vida en el examen. Memorízalas.

1. **Idempotencia:** $p \lor p \equiv p$  |  $p \land p \equiv p$
2. **Conmutativa:** $p \lor q \equiv q \lor p$  |  $p \land q \equiv q \land p$
3. **Leyes de Morgan (¡Fijas!):** $$\sim(p \land q) \equiv \sim p \lor \sim q$$
   $$\sim(p \lor q) \equiv \sim p \land \sim q$$
4. **Definición del Condicional (¡Muy usada!):** $$p \to q \equiv \sim p \lor q$$
5. **Leyes de Absorción (Ahorran minutos):**
   * $p \lor (p \land q) \equiv p$
   * $p \land (p \lor q) \equiv p$
   * $p \lor (\sim p \land q) \equiv p \lor q$ *(El de afuera absorbe a su negación)*
   * $p \land (\sim p \lor q) \equiv p \land q$

### 📝 Caso Práctico Resuelto: Simplificación
**Problema:** Simplificar la expresión: $\sim(\sim p \to q) \lor p$

**Solución Paso a Paso:**
1. Aplicamos la definición del condicional en el paréntesis ($A \to B \equiv \sim A \lor B$):
   $$\sim(\sim(\sim p) \lor q) \lor p$$
2. Doble negación ($\sim(\sim p) \equiv p$):
   $$\sim(p \lor q) \lor p$$
3. Aplicamos Ley de Morgan al paréntesis:
   $$(\sim p \land \sim q) \lor p$$
4. Aplicamos propiedad Conmutativa para acomodarlo a la vista:
   $$p \lor (\sim p \land \sim q)$$
5. Aplicamos Ley de Absorción (Caso 3: el de afuera absorbe a su negación interna):
   $$p \lor \sim q$$
   
**Respuesta:** La expresión se reduce a $p \lor \sim q$ (que también equivale a $q \to p$).

---

## [cite_start]6. Circuitos Lógicos 
Es la aplicación de la lógica a la física y electrónica.

### A. Circuito en Serie (Conjunción $\land$)
La energía debe pasar por todos los interruptores uno tras otro. Si uno falla, no hay corriente.
$$\text{--- } p \text{ --- } q \text{ ---} \equiv p \land q$$

### B. Circuito en Paralelo (Disyunción $\lor$)
La energía tiene caminos alternativos. Basta que un interruptor funcione para que pase la corriente.
$$\begin{matrix}
 \text{---} & p & \text{---} \\
 & | & \\
 \text{---} & q & \text{---} 
\end{matrix} \equiv p \lor q$$



### 📝 Caso Práctico Resuelto: Circuitos
**Problema:** Determinar la proposición que representa el siguiente circuito y simplificarla.
*(Imagina un circuito donde arriba hay un interruptor '$p$' y en paralelo, abajo, hay dos interruptores en serie '$\sim p$' y '$q$').*

**Solución Paso a Paso:**
1. **Traducción:** La rama de abajo está en serie, por lo tanto es $(\sim p \land q)$.
2. Esta rama inferior está en paralelo con el interruptor de arriba '$p$'. El paralelo es $\lor$.
3. La fórmula queda: $p \lor (\sim p \land q)$
4. **Simplificación:** Por la Ley de Absorción, esto es equivalente a:
   $$p \lor q$$

**Respuesta:** El circuito complejo equivale a un simple circuito en paralelo de $p$ y $q$.