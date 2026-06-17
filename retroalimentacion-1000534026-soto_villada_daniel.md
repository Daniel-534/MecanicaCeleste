# Retroalimentación de proyecto computacional

- Nombre completo: SOTO VILLADA DANIEL
- Cédula: 1000534026

## Archivos revisados

- Proyecto_AproximaciónApophis_MC2026_1.ipynb (versión final entregada)

## Historial de commits

- Repositorio original: https://github.com/Daniel-534/MecanicaCeleste
- Fecha de creación del repositorio: 2026-03-03 (antes del 14 de abril: si)
- Total de commits desde creación del repo: 118
- Primer commit: 2026-03-03
- Último commit: 2026-05-24
- Días activos con commits: 37
- Semanas activas con commits: 12
- Mayor pausa entre commits: 9 días

### Aplicación al repositorio

- Inicio oportuno: 5.0
- Constancia semanal: 5.0
- Regularidad: 5.0
- Iteración: 5.0
- Nota de ritmo de commits (promedio): 5.00 / 5.0

Interpretación breve: Ritmo muy constante y sostenible durante el semestre.

## Retroalimentación

- Archivo revisado: Proyecto_AproximaciónApophis_MC2026_1.ipynb (versión final entregada)

### Aspectos positivos

- El proyecto tiene un marco teórico formal que cubre el SSB, vectores de estado, el parámetro gravitacional μ y las ecuaciones del problema de N-cuerpos.
- Se obtienen condiciones iniciales de JPL Horizons para el Sol, todos los planetas y Apophis, haciendo buen uso de las herramientas del curso.
- Se integra la trayectoria del sistema completo con pymcel y se calcula correctamente la fecha (~14 de abril) y distancia de máxima aproximación (~80 793 km), comparándola con el valor de referencia.
- Se verifica la conservación de energía (variación del orden de 10⁻⁸) y se calcula el virial escalar y su derivada, constatando que el sistema satisface el teorema del virial.
- Hay celdas de análisis parciales después de los resultados principales que interpretan físicamente los hallazgos.

### Aspectos por mejorar

- No hay cálculo usando la teoría del problema de los dos cuerpos: trayectoria de Apophis con órbita kepleriana fija y estimación de la distancia mínima en ese modelo. [Parcialmente mejorado]
- No hay ninguna aplicación del problema de los tres cuerpos ni del CRTBP (problema circular restringido de tres cuerpos Sol-Tierra-Apophis). [Parcialmente mejorado]
- La discrepancia de ~100 % en distancia y 1 día en fecha no se analiza en profundidad; no se investiga cuántos cuerpos son necesarios para mejorar el resultado ni qué factores físicos explican la diferencia con la literatura. [Parcialmente mejorado]
- Varias celdas markdown actúan como simples títulos de bloque de código ("# Instalación de las librerías necesarias") en lugar de celdas narrativas con motivación física y ecuaciones que expliquen el experimento antes de ejecutarlo. [Parcialmente mejorado]
- Se observan celdas de código extensas; conviene modularizar más en funciones cortas y separar claramente las celdas de cálculo de las de graficación. [Parcialmente mejorado]
- No hay una sección final unificada de conclusiones que sintetice en 3–5 puntos los hallazgos físicos y computacionales del proyecto. [Parcialmente mejorado]

### Valoración global

- El trabajo tiene una base técnica sólida: integración N-cuerpos funcional, uso correcto de Horizons y verificación de cantidades conservadas. Sin embargo, el alcance es incompleto: faltan los bloques de dos cuerpos y tres cuerpos que son centrales en el curso, y la narrativa del notebook necesita desarrollarse para que funcione como un reporte científico.

## Valoración final

> Al no haber habido retroalimentación previa, el componente "Mejoras implementadas" se fusiona con "Aspectos positivos" (peso combinado 80 %).

- Aspectos positivos (primer entregable): 4.00 (80%)
- Aplicación al repositorio: 5.00 (10%)
- Valoración global: 3.00 (10%)

**Nota final (redondeada)**: 0.8×4.00 + 0.1×5.00 + 0.1×3.00 = (redondeado) 4.0
