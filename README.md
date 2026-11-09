# Introducción

El proyecto final del curso consistirá en la aplicación del aprendizaje por refuerzo para el mejoramiento o la automatización de un sistema específico. 

El trabajo del proyecto consiste en, dada la descripción del problema, definir los agentes de aprendizaje por refuerzo. El problema deberá ser implementado en su totalidad por los estudiantes. El desarrollo del proyecto seguirá las siguientes etapas:

1. Conformación de los equipos de trabajo
2. Diseño de la solución del problema definiendo el ambiente, acciones del agente y sistema de recompensas y definición de la estrategia (i.e., algoritmo) de solución.
3. Implementación de la solución, junto con casos de prueba y análisis de la solución.



# Distribución de entregas del proyecto

| **Semana 1 y 2**                        | **Semana 5**                                                                                                          | **Semana 8**                                                            |
| --------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| Constitución de los equipos de trabajo. | Entrega parcial del proyecto. Definición del ambiente de la aplicación del proyecto (estados, acciones, recompensas). | Entrega final del proyecto (ambiente y agente entrenado para ejecutar). |

# Entrega parcial del proyecto

Como punto intermedio del trabajo del proyecto, durante la semana 5 tendremos una entrega parcial. Para esta fecha se debe entregar una caracterización de su solución al proyecto. La caracterización del proyecto debe incluir:

- La definición del conjunto de estados del ambiente. Esta definición debe incluir una descripción explicita de los estados, tipo, rango de valores, otras características importantes.
- La definición de las acciones del agente. Definir explícitamente todas las acciones que puede ejecutar el agente. Para cada una de las acciones deben especificar los estados para las cuales la acción es aplicable.
- La función de recompensa, que debe definir exactamente cada una de las situaciones que ameritan una recompensa (parejas de estado, acción). Se debe especificar el valor numérico de las recompensas para las diferentes situaciones.

# Entrega final del proyecto

La entrega final del proyecto debe contener:

- Un video demostrando el funcionamiento de su solución del proyecto (la aplicación corriendo)
- La Q-tabla de los valores obtenidos para los estados y acciones
- El código completo de su solución (incluyendo las funciones para guardar y cargar la Q-tabla)



# Proyecto del curso

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/nHRq-5prRfSc11ZnKk2lPQ_f05d9d4d46a74893b774810f45e5b0f1_Banner_FINAL.jpg?expiry=1793407904376&hmac=d-STOhOwNUK5e2CKNbwF1LKFFzEW6t7dESfXtQJ7dQY)

Para el proyecto del curso vamos a construir un agente de RL para resolver un problema de aprendizaje específico. Para el proyecto deben ejecutar un agente de RL en el ambiente descrito a continuación, evaluar su ejecución y validar la efectividad del aprendizaje del agente entrenado sobre el ambiente.

Para esta tarea vamos a utilizar un ambiente dinámico donde el agente debe completar su tarea sin ser bloqueado por los obstáculos, los cuales se mueven aleatoriamente en cada paso. El objetivo del agente (el triangulo negro en la figura) es alcanzar el estado objetivo (el cuadrado verde en la parte inferior derecha de la figura) sin estrellarse con ninguno de los obstáculos (los círculos azules en la figura).

![471](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_a1099195cff34638b13f6c3055ccd381_Screenshot-2026-10-05-at-8.27.15-AM.png?expiry=1793407904376&hmac=14MbSjjkbkIerz9ydMw7CM532SYyO_Av0WdItg3aYIE)

El ambiente consiste de un cuarto de 8x8 vacía. El agente siempre se encuentra en la posición superior izquierda, la posición (0,0) del cuarto. El estado objetivo siempre se encuentra la posición inferior derecha, en la posición (7,7). Sin embargo, dentro del cuarto aparecen unos obstáculos de forma aleatoria (5 en total) los cuales deben ser evitados por el agente. El agente debe evitar los obstáculos en el ambiente, de estrellarse con alguno de ellos, el episodio se da por terminado.

En un pasó de la ejecución, los obstáculos cambian de posición a (posiblemente) una nueva posición, al mismo tiempo que el agente toma la decisión sobre la acción a tomar. El agente tiene dos grados de libertad para su movimiento, rotar sobre su eje 90º a la izquierda o derecha, o moverse a la casilla inmediatamente frente a él (si esto es posible).

Su misión es definir el problema (i.e., acciones, estados y sistema de recompensas) para permitir al agente alcanzar el objetivo. Entrenar al agente en el ambiente y poder explotar el entrenamiento para cargarlo en un agente. Además de esto su programa debe ser capaz de grabar la memoria del agente (i.e., la Q-tabla). Asegurese de guardar la información de las distintas pruebas que realice sobre el agente, para dejarlas ver en un pequeño reporte presentado los resultados.



# Nota y apuntes de sesiones de tutorías


Se debe describir y detallar cada una de las acciones

definir el sistemas de recompensa de manera detallada

los estados:
Posición del agente a  nivel de coordenadas y orientación
el agente no va a ver que tiene al frente, atras ni nada.
estado finalista o terminal toca definirlo.


Argumentación es la clave de esta entrega. explicar todo de manera mas posible clara

Se pueden agregar:
graficas
formulas
ilustraciones

giros del agente que considere necesarios

el agente si tiene que empezar en posición 0,0
los obstáculos  si tenemos libertad de elegir la posición inicial para que no empiecen en 0,0

En la funcion de accion (do accion) detertminar si cada uno de los obtaculos se muevan o no para que el movimiento sea simultaneo al agente.





No es necesario incluir la funcion de transición. 

sistema de recompesa:
jugar con recompensas negativas
recompensa cuando llega a un borde
recompensa cuando llega casilla blanca
recompensa cuando llega a la 7,7 super positiva



