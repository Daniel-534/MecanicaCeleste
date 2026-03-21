# La aproximación de Apophis en 2029

## Enunciado

En abril de 2029 el asteroide **(99942) Apophis** tendrá [una aproximación extrema con la Tierra](https://arxiv.org/pdf/2201.12205). Por el tamaño del asteroide, esta aproximación es considerada uno de los eventos astronómicos más importantes de esta década. En este proyecto usaremos la teoría, los métodos y los algorítmos vistos en el curso de Mecánica Celeste para estudiar la aproximación del asteroide.

El objetivo de este trabajo es que experimentes de primera mano lo que las personas expertas en mecánica celeste hacen cuando estudian las amenazas de asteroides. Aprovecha cada cosa que veas en el curso para crear un reporte científico que explore a fondo las características dinámicas de esta aproximación.

## Algunas ideas

Existen muchas maneras de aplicar la teoría que veremos en el curso en este problema y no queremos sesgar tu elección de los temas o cálculos que quieras escoger para aplicarla. Sin embargo aquí van algunas ideas de cálculos que se podrían hacer:
- Integración de la trayectoria del asteroide usando un integrador de N cuerpos y teniendo en cuenta los efectos de todos los planetas.
- Cálculo de la fecha y hora exacta de aproximación a la Tierra.
- Determinación de la distancia mínima de la órbita del asteroide a la órbita de la Tierra.
- Cálculo usando solo la teoría del problema de los dos cuerpos de la aproximación y comparación con la teoría de N cuerpos.
- Cálculo del cambio de la órbita heliocéntrica del asteroide después de su paso cerca de la Tierra.
- Aplicación de la teoría del problema de N cuerpos al asteroide.

En todos los casos debe ser evidente cómo estás usando los resultados teóricos que vemos en el curso.


## Entregables

El entregable del proyecto es **un notebook final de Jupyter** con una descripción de la teoría básica que uses, los experimentos numéricos que hayas realizado y las conclusiones a las que llegues con esos experimentos. Por supuesto puedes desarrollar otros programas y notebooks paralelos, pero se revisará el notebook con el reporte final.

Adicionalmente se deberá entregar **un repositorio de GitHub** que tenga todos los archivos, datos, notebooks, programas usados para este propósito. El notebook debe estar alojado en el repositorio.


## Criterios de evaluación

Una vez entregues el proyecto el profesor realizará una revisión del mismo y te lo devolverá con observaciones. En la segunda revisión emitirá un concepto cuantitativo del proyecto. Los criterios a evaluar serán:

- Correcta descripción y aplicación de la teoría.
- Originalidad de los experimentos numéricos.
- Conclusiones derivadas de los experimentos.
- Organización y extensión del reporte final.
- Ritmo de actualizaciones del repositorio de GitHub.

## Para tener en cuenta

- La solución presentada debe ser estrictamente individual. Evite resolver la tarea en parejas o en grupos que puede conducir a códigos o soluciones idénticos o muy similares.
- Los métodos y herramientas para resolver el problema deben ser los vistos en clase. El uso de herramientas diferentes puede ser una buena práctica en el mundo académico o laboral, pero en un curso puede también ser un indicio de un mal uso de las *asesorías* externa o del uso inapropiado de herramientas de Inteligencia Artificial (IA).
- El notebook entregado debe tener todos los resultados y gráficos, calculados y a la vista.  También debe ejecutarse completamente con `Ejecutar Todo` sin producir ningún error (verifique antes de entregar).
- El notebook debe tener explicaciones detalladas para cada paso del procedimiento usando celdas de texto. No debe poner una celda de código sin explicarla. En caso de incluir ecuaciones debe usar $\LaTeX$.


