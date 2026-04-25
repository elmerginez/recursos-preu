# 📘 Progresiones Aritméticas y Geométricas

---

## 🔷 1. Progresión Aritmética (PA)

Una progresión aritmética es una sucesión donde la diferencia entre términos consecutivos es constante.

### 📌 Fórmula general

\[
a_n = a_1 + (n-1)d
\]

- \( a_n \): término n-ésimo  
- \( a_1 \): primer término  
- \( d \): diferencia común  

---

### 🧠 Ejemplo básico

<div class="bg-gray-100 p-4 rounded-xl shadow-md">
<p>Si \( a_1 = 5 \) y \( d = 3 \):</p>

\[
a_2 = 5 + 3 = 8
\]
\[
a_3 = 8 + 3 = 11
\]
</div>

---

## 🔷 2. Progresión Aritmética Cuadrática

En este tipo, **la segunda diferencia es constante**.

### 📌 Forma general

\[
a_n = an^2 + bn + c
\]

### 🔍 Características

- No tiene diferencia constante.
- La diferencia de diferencias sí es constante.

---

### 🧠 Ejemplo

<div class="bg-blue-100 p-4 rounded-xl">
Secuencia: 2, 6, 12, 20, 30

Primera diferencia:
\[
4, 6, 8, 10
\]

Segunda diferencia:
\[
2, 2, 2
\]
✔ Es cuadrática
</div>

---

## 🔷 3. Progresión Aritmética Polinómica

Es una generalización donde la sucesión sigue un polinomio de grado mayor.

### 📌 Forma general

\[
a_n = a_k n^k + a_{k-1} n^{k-1} + \cdots + a_0
\]

### 🔍 Clave

- Si la diferencia de orden k es constante → es de grado k

---

### 🧠 Ejemplo cúbico

<div class="bg-green-100 p-4 rounded-xl">
Si la tercera diferencia es constante → polinomio grado 3
</div>

---

## 🔶 4. Progresión Geométrica (PG)

En una progresión geométrica, cada término se obtiene multiplicando por una constante.

### 📌 Fórmula

\[
a_n = a_1 \cdot r^{(n-1)}
\]

- \( r \): razón común

---

### 🧠 Ejemplo

<div class="bg-purple-100 p-4 rounded-xl shadow">
Si \( a_1 = 2 \) y \( r = 3 \):

\[
2, 6, 18, 54, ...
\]
</div>

---

## 📊 Comparación

<div class="grid grid-cols-2 gap-4">

<div class="bg-gray-200 p-4 rounded-lg">
<h3>Progresión Aritmética</h3>
<ul>
<li>Suma constante</li>
<li>Diferencia fija</li>
<li>Ej: 2, 5, 8, 11</li>
</ul>
</div>

<div class="bg-gray-200 p-4 rounded-lg">
<h3>Progresión Geométrica</h3>
<ul>
<li>Multiplicación constante</li>
<li>Razón fija</li>
<li>Ej: 2, 6, 18, 54</li>
</ul>
</div>

</div>

---

## 🧩 Resumen

<div class="bg-yellow-100 p-4 rounded-xl">
<ul>
<li>PA: diferencia constante</li>
<li>PA cuadrática: segunda diferencia constante</li>
<li>PA polinómica: diferencia de orden k constante</li>
<li>PG: razón constante</li>
</ul>
</div>

---

## ✨ Bonus: Fórmulas útiles

### Suma en PA
\[
S_n = \frac{n}{2}(a_1 + a_n)
\]

### Suma en PG
\[
S_n = a_1 \frac{r^n - 1}{r - 1}
\]

---
c