# Momento de Retroalimentación: Módulo 2 Análisis y Reporte sobre el desempeño del modelo
Dentro de este apartado se encuentra el primer entregable de mi portafolio de análisis respecto al módulo de Machine Learning, que básicamente consiste en el análsis y evaluación de un algoritmo de ML implementado por mi mismo para la entrega correspondiente al uso de un framework para un modelo de este estilo; utilicé redes neuronales apoyado de librerías como TensorFlow, Keras y ScikitLearn tanto para su implementación como para su refinamiento. Además, utilicé herramientas de apoyo como matplotlib para graficar y visualizar los datos correspondientes a pérdidas durante el entrenamiento y de validación, así como la implementación de GridSearch, una técnica muy utilizada, no solo para redes neuronales, sno también para distintos tipos de modelos de Machine Learning. Consiste en una búsqueda profunda en base a ciertas opciones de hiperparámetros que el usuario proporciona para que el algoritmo busqué la mejor configuración posible para algpun modelo de ML. Lo quer se busca en este entregable es analizar a profundidad si el algoritmo está realmente aprendiendo bien del contexto que está analizando y del que se encuentra produciendo estimaciones, para así corroborar su correcto o mal funcionamiento, de qué carece, tiene o no fallas, que puede mejorar y finalmente probar una nueva condiguración que pueda mejorar los resultados, como la métricas de error por ejemplo. Esta entrega se conforma de los siguientes archivos:
* <a href="https://github.com/4lb3rt0r/TC3006_Portafolio_Analisis/blob/main/final/M2_ML/An%C3%A1lisis%20y%20Reporte%20sobre%20el%20desempe%C3%B1o%20del%20modelo/Marvel_Movies.csv">**Marvel_Movies.csv:**</a> Datos de Películas de Marvel que han salido a lo largo de los años.
* <a href="https://github.com/4lb3rt0r/TC3006_Portafolio_Analisis/blob/main/final/M2_ML/An%C3%A1lisis%20y%20Reporte%20sobre%20el%20desempe%C3%B1o%20del%20modelo/Momento_de_Retroalimentaci%C3%B3n_An%C3%A1lisis_y_Reporte_sobre_el_desempe%C3%B1o_del_modelo.ipynb">**M2. Análisis y Reporte sobre el desempeño del modelo.ipynb:**</a> Jupyter Notebook donde se detalla más a profundidad el rendimiento y funcionamiento del algoritmo de redes neuronales implementado en entregas pasadas para el portafolio de implementación, dónde se explica a detalle si el modelo está aprendiendo, cómo se adapta al contexto de la base de datos proporcionada, es bueno o malo el modelo, qué tan fiable es, sufre de overfitting o underfitting y finalmente su refinamiento y posible ajuste:

1. Encabezado

    1.1 **Instrucciones e Información acerca del entregable:**

    Explicación breve sobre las instrucciones a seguir y un poco de contexto acerca de las herramientas a utilizar para este trabajo.

2. Análisis sobre el desempeño del algoritmo dentro del contexto:<br/>
   
   Reporte de análisis sobre el rendimiento de las redes neuronales utilizando datos del archivo "Marvel_Movies.csv", obtenidos de <a href="https://www.kaggle.com/datasets/joebeachcapital/marvel-movies">Kaggle</a> con información sobre películas de Marvel, incluye descripciones detalladas del uso de las herramientas de análisis, explicaciones y de los pasos que se siguieron para determinar el desempeño del modelo durante el proceso de entrenamiento, pruebas y validación, además de su refinamiento con una técina de GridSearch.

4. Gráfica:<br/>
   
   Graficación y tabulación de información utilizada durante el análisis posterior a la predicción y pruebas con el fin de visualizar el flujo de los datos, su comportamiento y su rendimiento para su posterior análisis y comprensión de los mismos.

## Cambios realizados con respecto a la entrega anterior
Se realizaron varias observaciones por parte del docente con respecto a la primera versión de este entregable, por lo cual, se realizaron ciertas modicaciones con el fin de cumplir con los criterios de la rúbrica que no se lograron alcanzar previamente. Es por ello que, a continuación se presentan las modificaciones realizadas al trabajo basados en la retroalimentación proporcionada por criterio faltante:

* **El reporte incluye una descripción breve de los datos incluidos en el dataset (cantidad de registros/muestras, número de características, número de clases de salida o rango de valores de salida).**
   * Ahora, el reporte incluye una descripción detallada del dataset utilizado para este entregable, así como una descripción por cada variable que conforma la base de datos con el fin de que el lector cuente con un recurso que le permita entender de mejor forma qué tipos de datos se están manejando y cómo está compuesto el dataset. Se especifíca con qué variable de entrada se va a trabajar para generar la variable de salida, que también se especifica dentro del mismo texto del reporte.

* **El conjunto de validación se utiliza para escoger el modelo final (refinamiento de hiper-parámetros).**
   * Esta métrica se resuelve al implementar dicho subset de validación de datos con el fin de que sea un complemento al subset de entrenamiento, y en base a los resultados que arroja el modelo con este subset de validación se determina aproximadamente cómo tiene que ser el refinamiento y la regularización de hiperparámetros y pesos.

* **El conjunto de prueba solamente se usa al final para reportar la capacidad de generalización del modelo seleccionado.**
   * El conjunto de pruebas ahora se usa solamente al final del reporte, no se utiliza en ningún otro lugar que no sea necesario.

* **Se detecta correctamente el grado de bias o sesgo: bajo medio alto.**
   * Ahora se deja más en claro el grado de bias gracias a la implementación de otro tipo de gráficas de apoyo con el fin de plasmar mejor las ideas que explican el comportamiento del modelo.

* **Se detecta correctamente el grado de varianza: bajo medio alto.**
   * Ahora se deja más en claro el grado de varianza gracias a la implementación de otro tipo de gráficas de apoyo con el fin de plasmar mejor las ideas que explican el comportamiento del modelo.

* **La decisión del grado de varianza se soporta con una tabla, gráfico, o similar.**
   * Ahora se deja más en claro el grado de varianza gracias a la implementación de otro tipo de gráficas de apoyo con el fin de plasmar mejor las ideas que explican el comportamiento del modelo.

* **Se detecta correctamente el nivel de ajuste del modelo: underfit, fit, overfit.**
   * Se tiene contemplado de forma más clara que el entregable anterior qué tipo de ajuste tiene el modelo de redes neuronales y se cuenta con material de apoyo como gráficas y datos que corroboran dicho estatuto.

* **La decisión del nivel de ajuste del modelo se soporta adecuadamente (explicación con base en criterior previos, o datos nuevos).**
   * Se incorpora una metodología un poco más sencilla y práctica que ayuda no solo a simplificar la forma en que se eligen modelos candidatos para su ajuste y refinamiento, sino que también se entiende de forma más clara el porqué se decidió variar o cambiar los hiperparámetros de una u otra forma.

* **Se utilizan técnicas de regularización para mejorar el desempeño del modelo.**
   * Se incorporó la técnica de regularización *l2* que, al menos en redes neuronales, sirve como una especie de "catalizador" de pesos sobre las neuronas del modelo, es decir, te permite manipular los pesos a tu gusto, reduce el overfitting del modelo y puede ayudar a mejorar la generalización 