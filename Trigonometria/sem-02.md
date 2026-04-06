# Semana 2: Razones Trigonométricas en el Triángulo Rectángulo

## Contenido
1. [Definición de las razones trigonométricas para ángulos agudos](#definición)
2. [Razones trigonométricas recíprocas](#recíprocas)
3. [Razones trigonométricas de ángulos complementarios](#complementarios)
4. [Razones trigonométricas de ángulos notables](#notables)
5. [Resolución de triángulos rectángulos](#resolución)
6. [Ejemplos integradores (básico a avanzado)](#ejemplos)

---

## 1. Definición de las razones trigonométricas para ángulos agudos <a name="definición"></a>

En un triángulo rectángulo, llamamos **ángulo agudo** a aquel que mide menos de 90° (o \(\frac{\pi}{2}\) rad). Para uno de estos ángulos, digamos \(\theta\), identificamos sus lados relativos:

- **Hipotenusa (h):** lado opuesto al ángulo recto, el más largo.
- **Cateto opuesto (CO):** lado que está enfrente de \(\theta\).
- **Cateto adyacente (CA):** lado que forma el ángulo \(\theta\) junto con la hipotenusa.

![Triángulo rectángulo](https://i.imgur.com/placeholder.png)  
*Descripción: triángulo rectángulo con ángulo θ, CO, CA e hipotenusa.*

Las seis razones trigonométricas se definen como:

| Razón | Símbolo | Fórmula |
|-------|---------|---------|
| Seno | \(\sin \theta\) | \(\frac{CO}{h}\) |
| Coseno | \(\cos \theta\) | \(\frac{CA}{h}\) |
| Tangente | \(\tan \theta\) | \(\frac{CO}{CA}\) |
| Cotangente | \(\cot \theta\) | \(\frac{CA}{CO}\) |
| Secante | \(\sec \theta\) | \(\frac{h}{CA}\) |
| Cosecante | \(\csc \theta\) | \(\frac{h}{CO}\) |

> **Regla mnemotécnica:** *SOH CAH TOA*  
> - **S**eno = **O**puesto / **H**ipotenusa  
> - **C**oseno = **A**dyacente / **H**ipotenusa  
> - **T**angente = **O**puesto / **A**dyacente

### Ejemplo básico
Dado un triángulo rectángulo con cateto opuesto a \(\theta = 3\), cateto adyacente = 4 e hipotenusa = 5. Calcular las seis razones para \(\theta\).

- \(\sin \theta = \frac{3}{5} = 0.6\)
- \(\cos \theta = \frac{4}{5} = 0.8\)
- \(\tan \theta = \frac{3}{4} = 0.75\)
- \(\cot \theta = \frac{4}{3} \approx 1.333\)
- \(\sec \theta = \frac{5}{4} = 1.25\)
- \(\csc \theta = \frac{5}{3} \approx 1.667\)

---

## 2. Razones trigonométricas recíprocas <a name="recíprocas"></a>

Las razones recíprocas son aquellas que al multiplicarse dan 1. Se cumplen las siguientes relaciones:

\[
\csc \theta = \frac{1}{\sin \theta}, \qquad
\sec \theta = \frac{1}{\cos \theta}, \qquad
\cot \theta = \frac{1}{\tan \theta}
\]

De manera inversa:
\[
\sin \theta = \frac{1}{\csc \theta}, \qquad
\cos \theta = \frac{1}{\sec \theta}, \qquad
\tan \theta = \frac{1}{\cot \theta}
\]

### Identidades por cociente
A partir de las definiciones también obtenemos:
\[
\tan \theta = \frac{\sin \theta}{\cos \theta}, \qquad
\cot \theta = \frac{\cos \theta}{\sin \theta}
\]

### Ejemplo intermedio
Si \(\sin \theta = 0.6\), hallar \(\csc \theta\), \(\sec \theta\) y \(\tan \theta\) (suponiendo un ángulo agudo en un triángulo 3-4-5).

- \(\csc \theta = \frac{1}{0.6} = \frac{5}{3} \approx 1.667\)
- Para \(\cos \theta\): usamos la identidad pitagórica \(\sin^2\theta + \cos^2\theta = 1\) → \(0.36 + \cos^2\theta = 1\) → \(\cos^2\theta = 0.64\) → \(\cos\theta = 0.8\) (positivo por ser agudo). Entonces \(\sec \theta = \frac{1}{0.8}=1.25\).
- \(\tan \theta = \frac{\sin\theta}{\cos\theta} = \frac{0.6}{0.8} = 0.75\).

---

## 3. Razones trigonométricas de ángulos complementarios <a name="complementarios"></a>

Dos ángulos agudos son **complementarios** si suman 90° (o \(\frac{\pi}{2}\) rad). En un triángulo rectángulo, los dos ángulos agudos siempre son complementarios. Si \(\alpha + \beta = 90^\circ\), entonces:

\[
\sin \alpha = \cos \beta, \quad
\tan \alpha = \cot \beta, \quad
\sec \alpha = \csc \beta
\]

Equivalentemente, para un ángulo \(\theta\) (agudo):
\[
\sin(90^\circ - \theta) = \cos \theta, \quad
\cos(90^\circ - \theta) = \sin \theta, \quad
\tan(90^\circ - \theta) = \cot \theta
\]
\[
\cot(90^\circ - \theta) = \tan \theta, \quad
\sec(90^\circ - \theta) = \csc \theta, \quad
\csc(90^\circ - \theta) = \sec \theta
\]

### Ejemplo
Calcular \(\sin 40^\circ\) sabiendo que \(\cos 50^\circ = 0.6428\).  
Como \(40^\circ + 50^\circ = 90^\circ\), entonces \(\sin 40^\circ = \cos 50^\circ = 0.6428\).

---

## 4. Razones trigonométricas de ángulos notables <a name="notables"></a>

Los ángulos de \(30^\circ\), \(45^\circ\) y \(60^\circ\) (y sus equivalentes en radianes \(\frac{\pi}{6},\frac{\pi}{4},\frac{\pi}{3}\)) aparecen frecuentemente. Sus razones se obtienen geométricamente:

### Triángulo equilátero (para 30° y 60°)
Dividiendo un triángulo equilátero de lado 2 por la altura, obtenemos un triángulo rectángulo con ángulos 30° y 60°, cateto opuesto a 30° = 1, hipotenusa = 2, cateto adyacente a 30° = \(\sqrt{3}\).

### Cuadrado (para 45°)
La diagonal de un cuadrado de lado 1 genera un triángulo rectángulo isósceles con catetos = 1 e hipotenusa = \(\sqrt{2}\). Sus ángulos agudos miden 45°.

### Tabla de valores exactos

| Ángulo | \(\sin\) | \(\cos\) | \(\tan\) | \(\cot\) | \(\sec\) | \(\csc\) |
|--------|----------|----------|----------|----------|----------|----------|
| \(30^\circ\) (\(\frac{\pi}{6}\)) | \(\frac{1}{2}\) | \(\frac{\sqrt{3}}{2}\) | \(\frac{\sqrt{3}}{3}\) | \(\sqrt{3}\) | \(\frac{2\sqrt{3}}{3}\) | \(2\) |
| \(45^\circ\) (\(\frac{\pi}{4}\)) | \(\frac{\sqrt{2}}{2}\) | \(\frac{\sqrt{2}}{2}\) | \(1\) | \(1\) | \(\sqrt{2}\) | \(\sqrt{2}\) |
| \(60^\circ\) (\(\frac{\pi}{3}\)) | \(\frac{\sqrt{3}}{2}\) | \(\frac{1}{2}\) | \(\sqrt{3}\) | \(\frac{\sqrt{3}}{3}\) | \(2\) | \(\frac{2\sqrt{3}}{3}\) |

> **Nota:** Los valores para \(37^\circ\) y \(53^\circ\) (aproximadamente 3-4-5) son útiles en problemas prácticos:  
> \(\sin 37^\circ \approx 0.6,\ \cos 37^\circ \approx 0.8,\ \tan 37^\circ \approx 0.75\)  
> \(\sin 53^\circ \approx 0.8,\ \cos 53^\circ \approx 0.6,\ \tan 53^\circ \approx 1.333\)

### Ejemplo con ángulos notables
Hallar el valor exacto de \(\tan 60^\circ + \sin 45^\circ \cdot \cos 30^\circ\).

\[
\tan 60^\circ = \sqrt{3}, \quad
\sin 45^\circ = \frac{\sqrt{2}}{2}, \quad
\cos 30^\circ = \frac{\sqrt{3}}{2}
\]
\[
\sin 45^\circ \cdot \cos 30^\circ = \frac{\sqrt{2}}{2} \cdot \frac{\sqrt{3}}{2} = \frac{\sqrt{6}}{4}
\]
\[
\text{Resultado} = \sqrt{3} + \frac{\sqrt{6}}{4}
\]

---

## 5. Resolución de triángulos rectángulos <a name="resolución"></a>

Resolver un triángulo rectángulo significa encontrar todos sus lados y ángulos desconocidos. Para ello usamos:

- **Teorema de Pitágoras:** \(h^2 = CO^2 + CA^2\)
- **Razones trigonométricas:** dependiendo de los datos conocidos.
- **Ángulos complementarios:** el tercer ángulo es \(90^\circ - \theta\).

### Casos típicos

#### Caso 1: Conocidos un ángulo agudo y la hipotenusa
Datos: \(\theta\) y \(h\).  
- \(CO = h \cdot \sin \theta\)  
- \(CA = h \cdot \cos \theta\)  
- Ángulo restante: \(90^\circ - \theta\)

#### Caso 2: Conocidos un ángulo agudo y un cateto
- Si se conoce \(\theta\) y \(CO\):  
  \(h = \frac{CO}{\sin \theta},\quad CA = \frac{CO}{\tan \theta}\)  
- Si se conoce \(\theta\) y \(CA\):  
  \(h = \frac{CA}{\cos \theta},\quad CO = CA \cdot \tan \theta\)

#### Caso 3: Conocidos dos catetos
Datos: \(CO\) y \(CA\).  
- \(h = \sqrt{CO^2 + CA^2}\)  
- \(\tan \theta = \frac{CO}{CA}\) → \(\theta = \arctan\left(\frac{CO}{CA}\right)\)  
- Ángulo complementario: \(90^\circ - \theta\)

#### Caso 4: Conocidos la hipotenusa y un cateto
Datos: \(h\) y \(CO\) (o \(CA\)).  
- El otro cateto por Pitágoras.  
- \(\sin \theta = \frac{CO}{h}\) → \(\theta = \arcsin\left(\frac{CO}{h}\right)\)  
- Ángulo complementario.

---

## 6. Ejemplos integradores (básico → avanzado) <a name="ejemplos"></a>

### Ejemplo 1 (Básico)
En un triángulo rectángulo, un cateto mide 5 cm y la hipotenusa 13 cm. Hallar las razones trigonométricas del ángulo opuesto al cateto de 5 cm.

**Solución:**  
Cateto opuesto = 5, hipotenusa = 13 → cateto adyacente = \(\sqrt{13^2 - 5^2} = \sqrt{169-25}= \sqrt{144}=12\).  
Para el ángulo \(\theta\) opuesto al lado de 5:
\[
\sin \theta = \frac{5}{13},\ \cos \theta = \frac{12}{13},\ \tan \theta = \frac{5}{12},\ \cot \theta = \frac{12}{5},\ \sec \theta = \frac{13}{12},\ \csc \theta = \frac{13}{5}.
\]

### Ejemplo 2 (Intermedio – complementarios)
Si \(\sin(2x+10^\circ) = \cos(3x-20^\circ)\) y los ángulos son agudos, hallar \(x\).

**Solución:**  
Para ángulos agudos, la igualdad \(\sin A = \cos B\) implica \(A + B = 90^\circ\).  
\[
(2x+10^\circ) + (3x-20^\circ) = 90^\circ \implies 5x -10^\circ = 90^\circ \implies 5x = 100^\circ \implies x = 20^\circ.
\]

### Ejemplo 3 (Intermedio – resolución con ángulos notables)
Desde la punta de un edificio, se observa un punto en el suelo con un ángulo de depresión de 30°. Si la altura del edificio es 50 m, ¿a qué distancia horizontal se encuentra el punto?

**Solución:**  
Ángulo de depresión = 30° ⇒ dentro del triángulo rectángulo, el ángulo agudo desde la horizontal es 30°.  
Cateto opuesto = altura = 50 m. Distancia horizontal \(d\) es el cateto adyacente.  
\[
\tan 30^\circ = \frac{\text{opuesto}}{\text{adyacente}} = \frac{50}{d} \implies d = \frac{50}{\tan 30^\circ} = \frac{50}{\frac{\sqrt{3}}{3}} = 50 \cdot \frac{3}{\sqrt{3}} = 50\sqrt{3} \approx 86.6\ \text{m}.
\]

### Ejemplo 4 (Avanzado – dos triángulos rectángulos superpuestos)
Un topógrafo mide el ángulo de elevación a la cima de una montaña desde dos puntos separados 200 m. Desde el primer punto el ángulo es 30°, desde el segundo (más cercano) es 45°. Si ambos puntos y la base de la montaña están en la misma línea horizontal, calcular la altura de la montaña.

**Solución:**  
Sea \(h\) la altura, \(x\) la distancia desde el segundo punto a la base. Entonces desde el primer punto la distancia es \(x+200\).  
\[
\tan 45^\circ = \frac{h}{x} \implies 1 = \frac{h}{x} \implies h = x.
\]  
\[
\tan 30^\circ = \frac{h}{x+200} \implies \frac{\sqrt{3}}{3} = \frac{h}{x+200}.
\]  
Sustituyendo \(h=x\): \(\frac{\sqrt{3}}{3} = \frac{x}{x+200}\). Resolviendo:  
\[
\sqrt{3}(x+200) = 3x \implies \sqrt{3}x + 200\sqrt{3} = 3x \implies 200\sqrt{3} = 3x - \sqrt{3}x = x(3-\sqrt{3})
\]  
\[
x = \frac{200\sqrt{3}}{3-\sqrt{3}}.
\]  
Racionalizamos: multiplicamos numerador y denominador por \(3+\sqrt{3}\):  
\[
x = \frac{200\sqrt{3}(3+\sqrt{3})}{9-3} = \frac{200\sqrt{3}(3+\sqrt{3})}{6} = \frac{100\sqrt{3}(3+\sqrt{3})}{3}.
\]  
Como \(h = x\), simplificamos:  
\[
h = 100\sqrt{3} + 100 = 100(\sqrt{3}+1) \approx 100(1.732+1)=273.2\ \text{m}.
\]

### Ejemplo 5 (Avanzado – identidades y ángulos notables)
Demostrar que \(\tan 15^\circ = 2 - \sqrt{3}\) usando ángulos complementarios y triángulos notables.

**Solución:**  
Observamos que \(15^\circ = 45^\circ - 30^\circ\). Aunque la fórmula de diferencia de tangentes se ve en semanas posteriores, podemos construir un triángulo rectángulo con ángulo 15°.  
Dibujamos un triángulo rectángulo con ángulos 15° y 75°. Tomamos la hipotenusa = 1. Entonces \(\sin 15^\circ\) y \(\cos 15^\circ\) se pueden obtener mediante identidades de medio ángulo (tema posterior), pero un método geométrico:  
Sobre un triángulo rectángulo isósceles (45-45-90) de catetos 1, se traza una línea que biseca un ángulo de 60°, etc. Sin embargo, una forma más simple es usar la relación \(\tan(45^\circ - 30^\circ)\) que se verá después, pero aceptamos que el resultado es conocido: \(\tan 15^\circ = 2 - \sqrt{3}\). Verificamos numéricamente: \(2 - 1.732 = 0.268\), y \(\tan 15^\circ \approx 0.268\).

---

## Resumen de fórmulas clave

| Concepto | Expresión |
|----------|------------|
| Seno | \(\sin \theta = \frac{CO}{h}\) |
| Coseno | \(\cos \theta = \frac{CA}{h}\) |
| Tangente | \(\tan \theta = \frac{CO}{CA}\) |
| Recíprocas | \(\csc \theta = \frac{1}{\sin \theta},\ \sec \theta = \frac{1}{\cos \theta},\ \cot \theta = \frac{1}{\tan \theta}\) |
| Complementarios | \(\sin(90^\circ-\theta)=\cos\theta,\ \tan(90^\circ-\theta)=\cot\theta\) |
| Pitágoras | \(\sin^2\theta + \cos^2\theta = 1\) |
| Ángulos notables | \(30^\circ, 45^\circ, 60^\circ\) con valores exactos dados en la tabla |

---

## Ejercicios propuestos (para practicar)

1. En un triángulo rectángulo, el cateto adyacente a un ángulo \(\alpha\) mide 8 cm y la hipotenusa 17 cm. Hallar las seis razones de \(\alpha\).
2. Si \(\tan \beta = 2.4\) y \(\beta\) es agudo, encontrar \(\sin \beta\) y \(\cos \beta\).
3. Simplificar: \(\sin 25^\circ \cdot \csc 25^\circ - \cos^2 40^\circ - \sin^2 40^\circ\).
4. Hallar el valor de \(x\) si \(\cos(3x-10^\circ) = \sin(2x+20^\circ)\).
5. Un avión vuela a 1200 m de altura y se acerca a un aeropuerto. El piloto mide un ángulo de depresión de 15° hacia la pista. ¿A qué distancia horizontal se encuentra el avión del punto de aterrizaje? (Usar \(\tan 15^\circ \approx 0.2679\)).

---

¡Con estos fundamentos estás listo para abordar aplicaciones más complejas como ángulos verticales, identidades y funciones trigonométricas!
