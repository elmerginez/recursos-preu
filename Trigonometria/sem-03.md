# Guía de Trigonometría: Ángulos Verticales y Horizontales

Este documento detalla el uso de ángulos de elevación, depresión, observación y sistemas de navegación (rumbos y azimut) para la resolución de problemas geométricos en 2D y 3D.

---

## 1. Ángulos Verticales

### Relación con Ángulo de Elevación (Nivel Intermedio)

Desde el objeto, el ángulo de elevación hacia el observador es **igual** al ángulo de depresión del observador hacia el objeto. Esto se debe a la propiedad de ángulos **alternos internos** entre líneas horizontales paralelas.



[Image of relationship between angle of elevation and angle of depression]


$$\alpha_{\text{elevación}} = \alpha_{\text{depresión}}$$

### Ejemplo 4 (Básico)
> Desde la cima de un faro de 40 m de altura, se observa un bote con un ángulo de depresión de 15°. ¿A qué distancia horizontal se encuentra el bote?

**Solución:**
Utilizamos la función tangente, donde la altura es el cateto opuesto y la distancia $d$ es el cateto adyacente:

$$\tan(15^\circ) = \frac{40}{d} \quad \Rightarrow \quad d = \frac{40}{\tan(15^\circ)}$$
$$d \approx \frac{40}{0.2679} \approx 149.3 \text{ m}$$

---

### Ejemplo 5 (Intermedio - Dos observadores)
> Desde dos puntos A y B en el suelo, separados 100 m, se observa un globo aerostático. Desde A el ángulo de elevación es 35°, desde B es 25°. Ambos puntos están alineados con la vertical del globo. Calcula la altura del globo.

**Solución:**
Sea $h$ la altura y $x$ la distancia de A al pie de la vertical.

1. $\tan(35^\circ) = \frac{h}{x}$
2. $\tan(25^\circ) = \frac{h}{100 + x}$



**Despejando $h$ e igualando:**
$$h = x \cdot \tan 35^\circ = (100 + x) \cdot \tan 25^\circ$$
$$x \cdot \tan 35^\circ - x \cdot \tan 25^\circ = 100 \cdot \tan 25^\circ$$
$$x (\tan 35^\circ - \tan 25^\circ) = 100 \cdot \tan 25^\circ$$

Sustituyendo $\tan 35^\circ \approx 0.7002$ y $\tan 25^\circ \approx 0.4663$:
$$x(0.2339) = 46.63 \Rightarrow x \approx 199.36 \text{ m}$$
$$h = 199.36 \cdot 0.7002 \approx \mathbf{139.6 \text{ m}}$$

---

## 2. Ángulo de Observación

El **ángulo de observación** (o ángulo visual) es el ángulo que subtiende un objeto en el ojo del observador. No se mide respecto a la horizontal, sino entre las visuales dirigidas a los extremos del objeto.

### Ejemplo 6 (Avanzado)
> Un observador ve un edificio. El ángulo de elevación a la parte superior es 40° y a la base es 10° (la base está por debajo del nivel del ojo). Si el observador está a 30 m de distancia horizontal, calcula la altura total del edificio.

**Solución:**
Dividimos la altura en $h_1$ (desde el nivel del ojo a la base) y $h_2$ (desde el nivel del ojo a la cima).

1. $\tan(10^\circ) = \frac{h_1}{30} \Rightarrow h_1 = 30 \cdot 0.1763 = 5.289 \text{ m}$
2. $\tan(40^\circ) = \frac{h_2}{30} \Rightarrow h_2 = 30 \cdot 0.8391 = 25.173 \text{ m}$

**Altura total:** $$H = h_1 + h_2 = 5.289 + 25.173 = \mathbf{30.46 \text{ m}}$$

---

## 3. Dirección y Rumbo (Ángulos Horizontales)

### 3.1 Rumbo (Bearing)
El rumbo es el ángulo agudo respecto al eje Norte-Sur. Se escribe como `[N/S] [Ángulo] [E/W]`.
* **N30°E:** Desde el norte, 30° hacia el este.

### 3.2 Dirección (Azimut)
Se mide desde el Norte en sentido horario, de 0° a 360°.

| Rumbo | Azimut |
|-------|--------|
| N $\alpha$ E | $\alpha$ |
| S $\alpha$ E | $180^\circ - \alpha$ |
| S $\alpha$ W | $180^\circ + \alpha$ |
| N $\alpha$ W | $360^\circ - \alpha$ |



### Ejemplo 4.3 (Problema con rumbos)
> Desde A, rumbo a B es N45°E (100 m). Desde B, rumbo a C es S60°E (80 m). Determinar distancia AC.

**Solución por componentes (A como origen):**
1. **Punto B:**
   - $x_B = 100 \cdot \sin 45^\circ \approx 70.71$
   - $y_B = 100 \cdot \cos 45^\circ \approx 70.71$
2. **Punto C (desde B):** S60°E equivale a un azimut de 120°.
   - $\Delta x = 80 \cdot \sin 120^\circ \approx 69.28$
   - $\Delta y = 80 \cdot \cos 120^\circ = -40$
3. **Coordenadas de C:**
   - $x_C = 70.71 + 69.28 = 139.99$
   - $y_C = 70.71 - 40 = 30.71$
4. **Distancia AC:**
   $$AC = \sqrt{139.99^2 + 30.71^2} \approx \mathbf{143.3 \text{ m}}$$

---

## 4. Problemas Mixtos (3D)

### Ejemplo 9 (Helicóptero)
> Desde O, se observa un helicóptero con elevación 30° y rumbo N40°E. Distancia inclinada = 800 m.

**Solución:**
1. **Altura ($z$):** $z = 800 \cdot \sin 30^\circ = 400 \text{ m}$
2. **Proyección en el suelo ($d$):** $d = 800 \cdot \cos 30^\circ \approx 692.8 \text{ m}$
3. **Componentes horizontales:**
   - $y (\text{Norte}) = d \cdot \cos 40^\circ \approx 530.7 \text{ m}$
   - $x (\text{Este}) = d \cdot \sin 40^\circ \approx 445.3 \text{ m}$

**Coordenadas:** $(445.3, 530.7, 400)$

---

## Resumen de Fórmulas Útiles

| Concepto | Fórmula |
|----------|---------|
| Ángulo de elevación | $\alpha = \arctan\left(\frac{h}{d}\right)$ |
| Componentes (Azimut $\theta$) | $x = d \cdot \sin\theta, \quad y = d \cdot \cos\theta$ |

---

## Ejercicios Propuestos

1. **Básico:** Elevación 42° desde 15 m. Hallar altura.
2. **Intermedio:** Avión a 2500 m, depresión 18°. Hallar distancia horizontal.
3. **Mixto:** Desde un faro de 60 m, depresión 12° y rumbo S70°O. Hallar coordenadas.
