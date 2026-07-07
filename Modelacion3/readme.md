# Dinámica de troyanos jovianos y la misión Lucy en el Problema Circular Restringido de Tres Cuerpos (CRTBP)

**Curso:** Mecánica Celeste — Instituto de Física, Facultad de Ciencias Exactas y Naturales, Universidad de Antioquia
**Autores** Soleil Niño, Sara Calle, Daniel Soto.
Junio 2026

## Descripción general

Este proyecto implementa el **Problema Circular Restringido de Tres Cuerpos (CRTBP)** aplicado al sistema Sol–Júpiter, usando como partículas de prueba a tres asteroides jovianos (**624 Hektor**, **153 Hilda**, **617 Patroclus**) y a la sonda espacial **Lucy** de la NASA.

A partir de efemérides reales obtenidas de **JPL Horizons**, se construyen condiciones iniciales en un marco inercial, se transforman al marco rotante baricéntrico del CRTBP y se expresan en unidades canónicas. Con ese marco se analizan las ecuaciones de movimiento, el potencial modificado y la **constante de Jacobi**, que permite identificar regiones dinámicamente permitidas y regiones de exclusión (superficies de cero velocidad) sin necesidad de integrar todas las trayectorias posibles.

El proyecto conecta la teoría clásica de la mecánica celeste (puntos de Lagrange, estabilidad de troyanos, resonancias) con un caso actual de exploración espacial: la navegación de Lucy por corredores dinámicos de baja energía rumbo a los troyanos de Júpiter.

## Contenido del repositorio y orden recomendado

El proyecto se presenta en varios formatos complementarios. Se recomienda revisarlos en este orden:

1. **Video y/o diapositivas** — Presentación resumida del proyecto: contexto, objetivos, metodología y resultados principales, explicados de forma narrativa. Es el mejor punto de partida para entender el "qué" y el "por qué" antes de entrar en el detalle técnico.
2. **Informe (LaTeX / PDF)** — Documento completo con el marco teórico, la metodología y el análisis de resultados. Aquí están las ecuaciones, las tablas de parámetros y la discusión detallada. Léelo después del video para profundizar en la formulación matemática y las decisiones metodológicas.
3. **Notebook (Jupyter)** — Implementación en Python, organizada de forma narrativa para reproducir todo el análisis: consulta de efemérides, transformación de coordenadas, cálculo de la constante de Jacobi y generación de las visualizaciones interactivas (trayectorias, mapas de potencial, regiones de exclusión). Ejecútalo al final para interactuar directamente con las figuras y ver el proceso completo paso a paso.

## Estructura teórica del informe

El informe (y por tanto el notebook) sigue esta estructura:

- **1. Introducción** — Contexto de los troyanos jovianos, la misión Lucy y los objetivos general y específicos del proyecto.
- **2. Marco teórico**
  - *Configuración del CRTBP Sol–Júpiter*: definición del parámetro de masa α y ubicación de los primarios en el marco rotante.
  - *Unidades canónicas*: normalización de masa, longitud, tiempo y velocidad para simplificar las ecuaciones.
  - *Ecuaciones de movimiento en el marco rotante*: incluye los términos gravitacionales, centrífugo y de Coriolis.
  - *Constante de Jacobi y regiones de exclusión*: la integral primera del CRTBP y su uso para definir superficies de cero velocidad.
- **3. Metodología**
  - Consulta de efemérides con JPL Horizons para el Sol, Júpiter, los tres asteroides y Lucy (intervalo del 16 de junio de 2026 al 16 de junio de 2027, paso de 5 días).
  - Transformación del marco inercial al marco rotante canónico (cálculo del baricentro, rotación por el ángulo Sol–Júpiter y adimensionalización).
  - Evaluación de regiones permitidas y prohibidas a partir de la constante de Jacobi de Lucy.
- **4. Resultados**
  - Parámetros canónicos del sistema Sol–Júpiter (α ≈ 9.54 × 10⁻⁴, unidades de longitud, tiempo y velocidad).
  - Estados iniciales adimensionales de cada cuerpo en el marco rotante.
  - Comparación de las constantes de Jacobi: Lucy presenta el valor más bajo (mayor acceso a regiones dinámicas abiertas), mientras que 153 Hilda presenta el valor más alto (mayor confinamiento).
  - Visualizaciones: trayectorias en el marco rotante, evolución temporal de la constante de Jacobi, mapa del potencial modificado y regiones de exclusión para Lucy.
- **5. Discusión** — Interpretación dinámica de los resultados, limitaciones del modelo (órbitas circulares, masas de prueba despreciables, sin perturbaciones adicionales ni maniobras de navegación) y trabajo futuro (modelo elíptico, integración N-cuerpo completa, análisis de cuellos dinámicos cerca de L1 y L2).
- **6. Conclusiones** — Síntesis de los hallazgos principales sobre la estabilidad de los puntos de Lagrange, la consistencia energética de la transformación al marco rotante y el mayor acceso dinámico de Lucy frente a los asteroides analizados.

## Requisitos para ejecutar el notebook

- Python 3.x con Jupyter.
- Librerías típicas de análisis numérico y visualización (numpy, matplotlib, y las necesarias para consultar JPL Horizons, según se especifique en el propio notebook).
- Conexión a internet si se desea repetir la consulta de efemérides en vivo.

## Referencias principales

- Giorgini et al. (1996). *JPL's On-Line Solar System Data Service.*
- Murray, C. D. y Dermott, S. F. (1999). *Solar System Dynamics.* Cambridge University Press.
- NASA (2026). *Lucy Mission.*
- NASA JPL (2026). *JPL Horizons On-Line Ephemeris System.*
- Szebehely, V. (1967). *Theory of Orbits: The Restricted Problem of Three Bodies.* Academic Press.
- Zuluaga, J. I. *Notas de mecánica celeste.* Material de curso, UdeA.
