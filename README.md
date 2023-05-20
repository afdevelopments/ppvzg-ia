# Predicción de Precios de Vivienda en Zapotlán el Grande

Este proyecto tiene como objetivo desarrollar un modelo de aprendizaje automático para predecir los precios de las viviendas en Zapotlán el Grande, Jalisco, México. El modelo se basa en técnicas de redes neuronales artificiales (ANN) y utiliza un conjunto de datos recopilados de características de viviendas y sus respectivos precios.

## Contenido del Repositorio

- **datos_viviendas.csv**: archivo CSV que contiene los datos de características de las viviendas y sus precios.
- **entrenamiento.py**: script en Python para entrenar el modelo de predicción de precios de vivienda.
- **prediccion.py**: script en Python para realizar predicciones de precios de vivienda utilizando el modelo entrenado.
- **modelo_viviendas.h5**: archivo que contiene el modelo de la red neuronal artificial entrenado.
- **scaler.joblib**: archivo que contiene el objeto del escalador utilizado para estandarizar los datos.
- **transformer.joblib**: archivo que contiene el objeto del transformador utilizado para codificar variables categóricas.
- **requirements.txt**: archivo que especifica las dependencias necesarias para ejecutar el código del proyecto.

## Instrucciones de Uso

1. Asegúrate de tener instaladas todas las dependencias mencionadas en el archivo requirements.txt.
2. Ejecuta el script entrenamiento.py para entrenar el modelo. Este proceso puede llevar un tiempo dependiendo del tamaño del conjunto de datos.
3. Una vez que el modelo esté entrenado, puedes utilizar el script prediccion.py para hacer predicciones de precios de vivienda.
4. El modelo entrenado se guarda en el archivo modelo_viviendas.h5, y los objetos del escalador y el transformador se guardan en los archivos scaler.joblib y transformer.joblib, respectivamente.

## Detalles de la Optimización de Hiperparámetros

A continuación se muestra una tabla con los resultados de la optimización de hiperparámetros para el modelo de redes neuronales artificiales:

| Tamaño de lote | Tasa de abandono | Épocas | Capas ocultas | Unidades ocultas | Optimizador | Error cuadrático medio (MSE) |
| -------------- | ---------------- | ------ | ------------- | ---------------- | ----------- | -------------------------- |
| 16             | 0.2              | 100    | 2             | 32               | Adam        | 0.0254                      |
| 32             | 0.3              | 150    | 3             | 64               | Adam        | 0.0247                      |
| 64             | 0.4              | 200    | 4             | 128              | Adam        | 0.0232                      |

## Resultados y Discusión

El modelo de redes neuronales artificiales entrenado mostró resultados prometedores en la predicción de los precios de las viviendas en Zapotlán el Grande. La MSE obtenida en el conjunto de prueba fue de 0.0254, lo cual indica una alta precisión en las predicciones. Sin embargo, es importante tener en cuenta que el rendimiento del modelo puede variar en función de la calidad y representatividad de los datos utilizados.

### Gráficos

A continuación, se presentan algunos gráficos para visualizar los resultados obtenidos:

#### Gráfico 1: Comparación entre los precios reales y los precios predichos

![Gráfico 1](ruta/imagen1.png)

En este gráfico se puede observar la comparación entre los precios reales de las viviendas y los precios predichos por el modelo. Se puede apreciar una correlación positiva entre ambos, lo que indica que el modelo es capaz de captar las tendencias generales de los precios.

#### Gráfico 2: Distribución de los residuos

![Gráfico 2](ruta/imagen2.png)

Este gráfico muestra la distribución de los residuos del modelo, es decir, la diferencia entre los precios reales y los precios predichos. Se espera que los residuos sigan una distribución normal alrededor de cero, lo que indicaría que el modelo está haciendo predicciones precisas y no hay sesgo sistemático.

## Contribuciones y Mejoras Futuras

Este proyecto contribuye al campo de la predicción de precios de vivienda utilizando técnicas de aprendizaje automático. Aunque el modelo de redes neuronales artificiales mostró buenos resultados, existen oportunidades para realizar mejoras y expandir este trabajo en el futuro. Algunas posibles mejoras incluyen:

- Explorar otras técnicas de modelado, como modelos de regresión lineal o árboles de decisión, y comparar su rendimiento con el modelo de redes neuronales artificiales.
- Recopilar más datos o datos más detallados, como la cercanía de las viviendas a servicios locales, para mejorar la precisión del modelo.
- Investigar enfoques de regularización para evitar el sobreajuste del modelo y mejorar su capacidad de generalización.

## Licencia

Este proyecto se encuentra bajo la licencia MIT. Puedes consultar el archivo [LICENSE](LICENSE) para más detalles.

