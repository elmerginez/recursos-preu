# Semana 1: Sistemas de Medición Angular, Longitud de Arco, Área del Sector Circular y Aplicaciones

## 1. Ángulo Trigonométrico

A diferencia del ángulo geométrico (limitado entre 0° y 180°), el **ángulo trigonométrico** se genera por la rotación de un rayo (lado inicial) alrededor de su origen (vértice) hasta una posición final (lado final). Puede ser:

- **Positivo**: si la rotación es en sentido contrario a las manecillas del reloj.
- **Negativo**: si la rotación es en sentido horario.
- **Ilimitado**: puede tomar cualquier valor real, mayor de 360° o menor de 0°.

### 1.1 Representación
En un plano cartesiano, el vértice se ubica en el origen y el lado inicial sobre el semieje positivo de las abscisas. El ángulo se denota con letras griegas como $\theta$, $\alpha$, $\beta$, etc.

![Ángulo trigonométrico](https://i.imgur.com/placeholder.png)  
*Imagen conceptual: rotación positiva y negativa.*

## 2. Sistemas de Medición Angular

Existen tres sistemas principales para medir ángulos:

| Sistema        | Unidad          | Símbolo | Equivalencia básica                     |
|----------------|-----------------|---------|------------------------------------------|
| Sexagesimal    | Grado sexagesimal | °       | 1 vuelta = 360°                          |
| Centesimal     | Grado centesimal  | g       | 1 vuelta = 400<sup>g</sup>               |
| Radial (Circular) | Radián          | rad     | 1 vuelta = $2\pi$ rad                    |

### 2.1 Sistema Sexagesimal (°)
- Un grado ($1^\circ$) equivale a $\frac{1}{360}$ de una vuelta completa.
- Submúltiplos:
  - $1^\circ = 60'$ (minutos)
  - $1' = 60''$ (segundos)
- Ejemplo: $23^\circ 15' 30''$

### 2.2 Sistema Centesimal (g)
- Un grado centesimal ($1^g$) equivale a $\frac{1}{400}$ de una vuelta.
- Submúltiplos:
  - $1^g = 100^m$ (minutos centesimales)
  - $1^m = 100^s$ (segundos centesimales)
- Es común en topografía e ingeniería civil.

### 2.3 Sistema Radial (rad)
- Un radián es el ángulo que, con vértice en el centro de una circunferencia, subtiende un arco de longitud igual al radio.
- Relación: $\text{ángulo (rad)} = \frac{\text{longitud de arco}}{\text{radio}}$
- Es el sistema natural en cálculo y trigonometría.

### 2.4 Equivalencias Fundamentales
$$ 180^\circ = \pi \text{ rad} = 200^g $$
De aquí se deducen los factores de conversión:

- De grados a radianes: $\text{rad} = \frac{\pi}{180^\circ} \times \text{grados}$
- De radianes a grados: $\text{grados} = \frac{180^\circ}{\pi} \times \text{rad}$
- De grados a centesimales: $^g = \frac{200^g}{180^\circ} \times \text{grados} = \frac{10}{9} \times \text{grados}$
- De centesimales a grados: $\text{grados} = \frac{180^\circ}{200^g} \times ^g = 0.9 \times ^g$

### 2.5 Tabla de Ángulos Notables

| Grados (°) | Radianes (rad) | Centesimales (g) |
|------------|----------------|------------------|
| 0°         | 0              | 0<sup>g</sup>    |
| 30°        | $\frac{\pi}{6}$ | $\frac{100}{3}^g \approx 33.333^g$ |
| 45°        | $\frac{\pi}{4}$ | 50<sup>g</sup>   |
| 60°        | $\frac{\pi}{3}$ | $\frac{200}{3}^g \approx 66.667^g$ |
| 90°        | $\frac{\pi}{2}$ | 100<sup>g</sup>  |
| 180°       | $\pi$           | 200<sup>g</sup>  |
| 270°       | $\frac{3\pi}{2}$| 300<sup>g</sup>  |
| 360°       | $2\pi$          | 400<sup>g</sup>  |

### 2.6 Ejemplos de Conversión

**Ejemplo 1:** Convertir $47^\circ$ a radianes.  
Solución: $\theta_{rad} = 47^\circ \times \frac{\pi}{180^\circ} = \frac{47\pi}{180} \text{ rad}$.

**Ejemplo 2:** Convertir $\frac{5\pi}{12}$ rad a grados.  
Solución: $\theta_{grados} = \frac{5\pi}{12} \times \frac{180^\circ}{\pi} = 75^\circ$.

**Ejemplo 3:** Expresar $125^g$ en grados sexagesimales.  
Solución: $125^g \times \frac{180^\circ}{200^g} = 125 \times 0.9 = 112.5^\circ = 112^\circ 30'$.

**Ejemplo 4:** Si un ángulo mide $2.5$ rad, ¿cuántos grados centesimales son?  
Solución: Primero a grados: $2.5 \times \frac{180^\circ}{\pi} \approx 143.239^\circ$. Luego a centesimales: $143.239^\circ \times \frac{200^g}{180^\circ} \approx 159.154^g$.

## 3. Longitud de Arco de una Circunferencia

Dada una circunferencia de radio $R$ y un ángulo central $\theta$ (medido en **radianes**), la longitud del arco $L$ que subtiende es:

$$ L = R \cdot \theta $$

**Demostración:** La longitud de toda la circunferencia es $2\pi R$ y corresponde a un ángulo de $2\pi$ rad. Por regla de tres:  
$\frac{L}{2\pi R} = \frac{\theta}{2\pi} \Rightarrow L = R\theta$.

> **Importante:** La fórmula solo es válida si $\theta$ está en radianes. Si el ángulo está en grados o centesimales, primero convertir a radianes.

### 3.1 Ejemplos

**Ejemplo 1:** Calcular la longitud de arco para $R = 5$ cm y $\theta = 60^\circ$.  
Solución: Convertimos $\theta$ a rad: $60^\circ \times \frac{\pi}{180} = \frac{\pi}{3}$ rad.  
$L = 5 \cdot \frac{\pi}{3} = \frac{5\pi}{3} \approx 5.236$ cm.

**Ejemplo 2:** Un arco mide $12$ m y el radio es $8$ m. Hallar el ángulo central en grados.  
Solución: $\theta_{rad} = \frac{L}{R} = \frac{12}{8} = 1.5$ rad.  
A grados: $1.5 \times \frac{180^\circ}{\pi} \approx 85.94^\circ$.

**Ejemplo 3:** Una rueda de radio $0.4$ m gira $3.2$ rad. ¿Qué distancia recorre un punto en la periferia?  
Solución: $L = R\theta = 0.4 \times 3.2 = 1.28$ m. (Distancia lineal recorrida por el punto).

## 4. Área de un Sector Circular

El sector circular es la región limitada por dos radios y el arco correspondiente. Su área $A$ se calcula con:

$$ A = \frac{1}{2} R^2 \theta $$

donde $\theta$ está en radianes. También puede expresarse como $A = \frac{L \cdot R}{2}$, siendo $L$ la longitud de arco.

**Demostración:** El área del círculo completo es $\pi R^2$ para un ángulo de $2\pi$ rad. Por proporción: $\frac{A}{\pi R^2} = \frac{\theta}{2\pi} \Rightarrow A = \frac{1}{2}R^2\theta$.

### 4.1 Ejemplos

**Ejemplo 1:** Calcular el área de un sector con $R = 10$ cm y $\theta = 2$ rad.  
Solución: $A = \frac{1}{2} (10)^2 (2) = \frac{1}{2} \cdot 100 \cdot 2 = 100$ cm².

**Ejemplo 2:** Un sector tiene área $30$ m² y radio $6$ m. Hallar el ángulo central en grados.  
Solución: Despejamos $\theta = \frac{2A}{R^2} = \frac{2 \cdot 30}{36} = \frac{60}{36} = \frac{5}{3}$ rad.  
En grados: $\frac{5}{3} \cdot \frac{180^\circ}{\pi} = \frac{300^\circ}{\pi} \approx 95.49^\circ$.

**Ejemplo 3:** (Aplicación) Una pizza de $30$ cm de diámetro se corta en $8$ porciones iguales. ¿Área de cada porción?  
Solución: Radio $R = 15$ cm. Ángulo por porción: $360^\circ/8 = 45^\circ = \frac{\pi}{4}$ rad.  
$A = \frac{1}{2}(15)^2 \cdot \frac{\pi}{4} = \frac{225\pi}{8} \approx 88.36$ cm².

## 5. Número de Vueltas de una Rueda sin Resbalar

Cuando una rueda rueda sin deslizar sobre una superficie, la distancia lineal recorrida por su centro es igual a la longitud de arco recorrida por un punto del borde. Si la rueda da $n$ vueltas completas, el ángulo girado es $\theta = 2\pi n$ (radianes). La distancia $d$ recorrida es:

$$ d = n \cdot (2\pi R) = n \cdot \text{circunferencia} $$

Por lo tanto, el número de vueltas se obtiene como:

$$ n = \frac{d}{2\pi R} $$

También, si se conoce el ángulo girado $\theta$ (en radianes): $n = \frac{\theta}{2\pi}$.

### 5.1 Ejemplos

**Ejemplo 1:** Una rueda de $0.5$ m de radio recorre $100$ m. ¿Cuántas vueltas da?  
Solución: $n = \frac{100}{2\pi(0.5)} = \frac{100}{\pi} \approx 31.83$ vueltas.

**Ejemplo 2:** Una rueda gira $1200^\circ$. Calcular las vueltas.  
Solución: Convertir a rad: $1200^\circ \times \frac{\pi}{180} = \frac{20\pi}{3}$ rad.  
$n = \frac{20\pi/3}{2\pi} = \frac{20}{6} = \frac{10}{3} \approx 3.333$ vueltas.

**Ejemplo 3:** Un vehículo tiene ruedas de $70$ cm de diámetro. Si da $500$ vueltas, ¿qué distancia recorre?  
Solución: Radio $= 0.35$ m. $d = 500 \times (2\pi \times 0.35) = 500 \times 0.7\pi = 350\pi \approx 1099.56$ m.

## 6. Relación entre Ruedas (Transmisión de Movimiento)

En sistemas de engranajes, poleas o ruedas de fricción, la transmisión de movimiento puede ocurrir de dos formas principales:

### 6.1 Mismo Eje (Ruedas solidarias)
Varias ruedas fijas al mismo eje giran con la misma **velocidad angular** $\omega$ (mismo ángulo en el mismo tiempo). Por lo tanto, el número de vueltas de todas es idéntico.

### 6.2 Transmisión por Contacto o Correa
Si dos ruedas están en contacto (sin deslizar) o unidas por una correa inextensible, la **velocidad lineal** $v$ en la periferia es la misma para ambas. Como $v = \omega R$, se cumple:

$$ \omega_1 R_1 = \omega_2 R_2 \quad \Rightarrow \quad \frac{\omega_1}{\omega_2} = \frac{R_2}{R_1} $$

En términos de número de vueltas $n$ en un tiempo dado: $\frac{n_1}{n_2} = \frac{R_2}{R_1}$.

**Consecuencia:** La rueda de menor radio gira más rápido (más vueltas).

### 6.3 Ejemplos

**Ejemplo 1:** Dos ruedas de radios $R_1 = 10$ cm y $R_2 = 25$ cm están conectadas por una correa. Si la rueda pequeña da $40$ vueltas, ¿cuántas vueltas da la grande?  
Solución: $n_1 R_1 = n_2 R_2$ (por igualdad de arcos recorridos: $2\pi R_1 n_1 = 2\pi R_2 n_2$).  
$n_2 = n_1 \cdot \frac{R_1}{R_2} = 40 \cdot \frac{10}{25} = 16$ vueltas.

**Ejemplo 2:** Dos engranajes tienen $20$ y $60$ dientes. Si el primero gira a $300$ rpm, ¿a qué rpm gira el segundo?  
Solución: El número de dientes es proporcional al radio (mismo módulo). $n_1 \cdot \text{dientes}_1 = n_2 \cdot \text{dientes}_2$ (la velocidad de giro es inversamente proporcional al número de dientes).  
$n_2 = 300 \cdot \frac{20}{60} = 100$ rpm.

**Ejemplo 3:** Un sistema de poleas tiene una polea motriz de radio $0.2$ m y una conducida de $0.5$ m. Si la motriz da $150$ vueltas, ¿cuántos radianes gira la conducida?  
Solución: $n_2 = 150 \cdot \frac{0.2}{0.5} = 60$ vueltas. Ángulo en rad: $60 \times 2\pi = 120\pi$ rad.

## 7. Problemas Resueltos de Aplicación (Básico a Avanzado)

### Problema 1 (Conversión de sistemas)
Tres ángulos $A$, $B$ y $C$ miden respectivamente $40^g$, $\frac{\pi}{5}$ rad y $36^\circ$. Ordenarlos de menor a mayor.  
**Solución:**  
- $A = 40^g = 40 \times 0.9^\circ = 36^\circ$  
- $B = \frac{\pi}{5}$ rad $= \frac{180^\circ}{5} = 36^\circ$  
- $C = 36^\circ$  
Los tres son iguales.

### Problema 2 (Longitud de arco y área)
En una circunferencia de radio $8$ cm, se tiene un sector circular cuyo arco mide $12$ cm. Calcular: a) el ángulo central en radianes, b) el área del sector.  
**Solución:**  
a) $\theta = \frac{L}{R} = \frac{12}{8} = 1.5$ rad.  
b) $A = \frac{1}{2} R^2 \theta = \frac{1}{2} \cdot 64 \cdot 1.5 = 48$ cm².

### Problema 3 (Número de vueltas con cambio de radio)
Una bicicleta tiene una rueda delantera de $0.35$ m de radio y una trasera de $0.40$ m. Si la rueda trasera da $200$ vueltas, ¿cuántas vueltas da la delantera? (Ambas ruedas recorren la misma distancia porque están en el mismo vehículo).  
**Solución:** Distancia recorrida por la trasera: $d = 200 \cdot 2\pi (0.40) = 160\pi$ m.  
Vueltas delantera: $n_d = \frac{d}{2\pi (0.35)} = \frac{160\pi}{0.7\pi} = \frac{160}{0.7} \approx 228.57$ vueltas.

### Problema 4 (Ruedas conectadas por correa con deslizamiento nulo)
Dos poleas de radios $15$ cm y $45$ cm están unidas por una correa. Si la polea pequeña gira a $120$ rpm, calcular: a) la velocidad angular de la grande en rad/s, b) la velocidad lineal de la correa en m/s.  
**Solución:**  
a) $n_2 = n_1 \cdot \frac{R_1}{R_2} = 120 \cdot \frac{15}{45} = 40$ rpm.  
Para convertir a rad/s: $40 \frac{\text{rev}}{\text{min}} \times \frac{2\pi \text{ rad}}{1 \text{ rev}} \times \frac{1 \text{ min}}{60 \text{ s}} = \frac{80\pi}{60} = \frac{4\pi}{3} \approx 4.1888$ rad/s.  
b) Velocidad lineal $v = \omega_1 R_1 = \left(120 \cdot \frac{2\pi}{60}\right) \times 0.15 = (4\pi) \times 0.15 = 0.6\pi \approx 1.884$ m/s.

### Problema 5 (Área de sector y aplicación a ingeniería)
Una cinta transportadora pasa por una polea de radio $0.2$ m que gira un ángulo de $240^\circ$. Calcular la longitud de cinta en contacto con la polea (arco de contacto) y el área de la sección de la polea cubierta por la cinta.  
**Solución:**  
$\theta = 240^\circ = 240 \cdot \frac{\pi}{180} = \frac{4\pi}{3}$ rad.  
Longitud de arco $L = 0.2 \cdot \frac{4\pi}{3} = \frac{0.8\pi}{3} \approx 0.8378$ m.  
Área del sector (vista lateral de la polea cubierta): $A = \frac{1}{2}(0.2)^2 \cdot \frac{4\pi}{3} = 0.02 \cdot \frac{4\pi}{3} = \frac{0.08\pi}{3} \approx 0.08378$ m².

## 8. Ejercicios Propuestos para Practicar

1. Expresar $150^\circ$ en radianes y en grados centesimales.
2. Un arco de circunferencia mide $25$ cm y el radio es $10$ cm. Hallar el ángulo central en grados sexagesimales.
3. Una rueda de $0.6$ m de diámetro recorre $1.2$ km. ¿Cuántas vueltas da?
4. Calcular el área de un sector circular con radio $12$ cm y ángulo $2.5$ rad.
5. Dos ruedas están conectadas por una correa. La mayor tiene radio $30$ cm y gira a $60$ rpm. ¿A qué velocidad angular (en rad/s) gira la menor si su radio es $10$ cm?
6. Un tractor tiene ruedas delanteras de $1.2$ m de diámetro y traseras de $1.6$ m. Si las traseras dan $80$ vueltas, ¿cuántas vueltas dan las delanteras? (Mismo desplazamiento).

## 9. Resumen de Fórmulas Clave

| Concepto               | Fórmula (condiciones)                       |
|------------------------|----------------------------------------------|
| Conversión grados ↔ rad | $\theta_{rad} = \theta_{grad} \cdot \frac{\pi}{180}$ |
| Longitud de arco       | $L = R \theta$ (θ en rad)                   |
| Área de sector         | $A = \frac{1}{2} R^2 \theta$ (θ en rad)     |
| Vueltas de una rueda   | $n = \frac{d}{2\pi R} = \frac{\theta}{2\pi}$ |
| Transmisión por correa | $n_1 R_1 = n_2 R_2$  (misma $v$ lineal)     |

> **Nota final:** Dominar estos conceptos es fundamental para el estudio de funciones trigonométricas, movimiento circular y aplicaciones en ingeniería mecánica, civil y eléctrica.
