# Clase 17: El Problema Relativo de Dos Cuerpos – Solución Analítica y el Plano de Laplace

## 1. Reducción al Plano de la Trayectoria (Plano de Laplace)

Partimos del conteo de cuadraturas obtenidas en el espacio tridimensional:
- M.A.R.E. ($\vec{h}$): 3 componentes
- E.R.E. ($\mathcal{E}$): 1 escalar
- Vector de Laplace ($\vec{e}$): 3 componentes
Total: 7 constantes, menos 1 ligadura ($\vec{h} \cdot \vec{e} = 0$) = 6 cuadraturas independientes.

Al pasar al **plano de la trayectoria** (plano orbital perpendicular a $\vec{h}$), el problema se reduce a 2 dimensiones espaciales. En este plano, el número de variables dinámicas independientes es 4 ($x, y, \dot{x}, \dot{y}$), por lo que solo necesitamos 4 cuadraturas:
1. $h = |\vec{h}|$ (módulo del momento angular específico)
2. $\mathcal{E}$ (energía relativa específica)
3. Dirección de $\vec{e}$ en el plano (1 cuadratura angular)
4. Módulo de $\vec{e}$ (1 cuadratura escalar)

Este marco permite enfocarse exclusivamente en la geometría y dinámica plana de la órbita.

---

## 2. Análisis del Vector de Laplace ($\vec{e}$)

El vector se define como:
$$\vec{e} = \frac{\vec{v} \times \vec{h}}{\mu} - \frac{\vec{r}}{r}$$

### 2.1 Dirección y significado geométrico
- $\vec{e}$ es constante en magnitud y dirección.
- Se encuentra contenido en el plano orbital, ya que es combinación lineal de $\vec{r}$ y $\vec{v}$.
- **Interpretación:** El vector $\vec{e}$ apunta siempre hacia el **periastro** (punto de mínima distancia radial). El ángulo $\theta$ medido desde la dirección de $\vec{e}$ hasta $\vec{r}$ se denomina *verdadera anomalía*.

### 2.2 Cálculo de la magnitud $e^2$
Calculamos el producto escalar $\vec{e} \cdot \vec{e}$ para obtener una expresión analítica en función de las integrales del movimiento:
$$e^2 = \left( \frac{\vec{v} \times \vec{h}}{\mu} - \frac{\vec{r}}{r} \right) \cdot \left( \frac{\vec{v} \times \vec{h}}{\mu} - \frac{\vec{r}}{r} \right)$$
Desarrollando:
$$e^2 = \frac{|\vec{v} \times \vec{h}|^2}{\mu^2} - \frac{2}{\mu r} (\vec{v} \times \vec{h}) \cdot \vec{r} + 1$$

**Paso A. Primer término (Identidad de Lagrange):**
$$|\vec{v} \times \vec{h}|^2 = v^2 h^2 - (\vec{v} \cdot \vec{h})^2$$
Dado que $\vec{h} = \vec{r} \times \vec{v}$, entonces $\vec{v} \cdot \vec{h} = 0$. Por tanto:
$$|\vec{v} \times \vec{h}|^2 = v^2 h^2$$

**Paso B. Segundo término (Propiedad cíclica del triple producto escalar):**
$$(\vec{v} \times \vec{h}) \cdot \vec{r} = \vec{h} \cdot (\vec{r} \times \vec{v}) = \vec{h} \cdot \vec{h} = h^2$$

**Paso C. Ensamblaje y sustitución de la energía:**
$$e^2 = \frac{v^2 h^2}{\mu^2} - \frac{2 h^2}{\mu r} + 1 = 1 + \frac{2h^2}{\mu^2} \left( \frac{v^2}{2} - \frac{\mu}{r} \right)$$
Reconociendo $\mathcal{E} = \frac{v^2}{2} - \frac{\mu}{r}$, obtenemos:
$$\boxed{e^2 = 1 + \frac{2\mathcal{E}h^2}{\mu^2}}$$

### 2.3 Clasificación de órbitas según la energía
La relación anterior vincula directamente la geometría de la cónica con la energía del sistema:
- Si $\mathcal{E} < 0 \Rightarrow 0 \le e < 1$: Órbita cerrada (**Elipse**)
- Si $\mathcal{E} = 0 \Rightarrow e = 1$: Órbita límite de escape (**Parábola**)
- Si $\mathcal{E} > 0 \Rightarrow e > 1$: Órbita abierta (**Hipérbola**)

---

## 3. Deducción de la Ecuación Polar de la Trayectoria

Proyectamos el vector de Laplace sobre el vector posición $\vec{r}$ para obtener la relación funcional entre $r$ y $\theta$.

**Paso 1. Proyección geométrica:**
$$\vec{e} \cdot \vec{r} = e r \cos\theta$$
donde $\theta$ es el ángulo entre $\vec{e}$ y $\vec{r}$ (verdadera anomalía).

**Paso 2. Proyección algebraica (usando la definición de $\vec{e}$):**
$$\vec{e} \cdot \vec{r} = \left( \frac{\vec{v} \times \vec{h}}{\mu} - \frac{\vec{r}}{r} \right) \cdot \vec{r} = \frac{(\vec{v} \times \vec{h}) \cdot \vec{r}}{\mu} - \frac{\vec{r} \cdot \vec{r}}{r}$$
Usando $(\vec{v} \times \vec{h}) \cdot \vec{r} = h^2$ y $\vec{r} \cdot \vec{r} = r^2$:
$$\vec{e} \cdot \vec{r} = \frac{h^2}{\mu} - r$$

**Paso 3. Igualación y despeje de $r(\theta)$:**
$$e r \cos\theta = \frac{h^2}{\mu} - r$$
$$r(1 + e \cos\theta) = \frac{h^2}{\mu}$$
Definiendo el **parámetro semilatus rectum** $p \equiv \frac{h^2}{\mu}$, llegamos a la ecuación final:
$$\boxed{r(\theta) = \frac{p}{1 + e \cos\theta}}$$

---

## 4. Resumen de la Integración Completa

1. El problema relativo de dos cuerpos posee 6 cuadraturas independientes que lo hacen completamente integrable.
2. En el plano orbital, estas se condensan en 4 constantes escalares: $h$, $\mathcal{E}$, la dirección de $\vec{e}$ y su magnitud $e$.
3. El vector $\vec{e}$ fija la orientación de la órbita (apunta al periastro) y su módulo determina la excentricidad geométrica mediante $e^2 = 1 + \frac{2\mathcal{E}h^2}{\mu^2}$.
4. La proyección de $\vec{e}$ sobre $\vec{r}$ conduce directamente a $r(\theta) = \frac{p}{1 + e \cos\theta}$, demostrando analíticamente que la trayectoria relativa es siempre una sección cónica con un foco en el origen del sistema relativo.

Este desarrollo cierra la solución analítica del problema de dos cuerpos y establece las bases para el estudio de la geometría de las cónicas y su representación en sistemas de referencia observacionales.
