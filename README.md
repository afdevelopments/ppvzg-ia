# Predicción de Precios de Vivienda en Zapotlán el Grande

Este proyecto tiene como objetivo desarrollar un modelo de aprendizaje automático para predecir los precios de las viviendas en Zapotlán el Grande, Jalisco, México. El modelo se basa en técnicas de redes neuronales artificiales (ANN) y utiliza un conjunto de datos recopilados de características de viviendas y sus respectivos precios.

## Contribuidores

- Luis Fernando Chavez Jiménez ([GitHub](https://github.com/Tobiny))
- Guillermo Moreno Rivera ([GitHub](https://github.com/Mim0518))
- César Joel Ramirez Maciel ([GitHub](https://github.com/Cesar-Joel))

## Repositorio

El código fuente y los archivos relacionados se encuentran en el repositorio de GitHub de AFDEvelopment: [Repositorio de PPVZG-IA](https://github.com/afdevelopments/ppvzg-ia)

## Contenido del Repositorio

- **datos_viviendas.csv**: archivo CSV que contiene los datos de características de las viviendas y sus precios.
- **entrenamiento.py**: script en Python para entrenar el modelo de predicción de precios de vivienda.
- **prediccion.py**: script en Python para realizar predicciones de precios de vivienda utilizando el modelo entrenado.
- **modelo_viviendas.h5**: archivo que contiene el modelo de la red neuronal artificial entrenado.
- **scaler.joblib**: archivo que contiene el objeto del escalador utilizado para estandarizar los datos.
- **transformer.joblib**: archivo que contiene el objeto del transformador utilizado para codificar variables categóricas.
- **requirements.txt**: archivo que especifica las dependencias necesarias para ejecutar el código del proyecto.

## Requisitos de Instalación

1. Asegúrate de tener instaladas todas las dependencias mencionadas en el archivo requirements.txt. Puedes instalarlas ejecutando el siguiente comando:

```pip install -r requirements.txt```

## Instrucciones de Uso

1. Ejecuta el script `entrenamiento.py` para entrenar el modelo. Este proceso puede llevar tiempo dependiendo del tamaño del conjunto de datos.

```python entrenamiento.py```

2. Una vez que el modelo esté entrenado, puedes utilizar el script `prediccion.py` para hacer predicciones de precios de vivienda.

```python prediccion.py```


3. El modelo entrenado se guarda en el archivo `modelo_viviendas.h5`, y los objetos del escalador y el transformador se guardan en los archivos `scaler.joblib` y `transformer.joblib`, respectivamente.

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

#### Gráfico 1: Pérdida durante el entrenamiento

![Gráfico 1](images/perdida_entrenamiento.png)

En este gráfico se muestra la evolución de la pérdida durante el entrenamiento del modelo a lo largo de las épocas. Se puede observar que la pérdida disminuye a medida que avanzan las épocas, lo que indica que el modelo está aprendiendo de manera efectiva.

#### Gráfico 2: Pérdida durante la validación

![Gráfico 2](images/perdida_validacion.png)

En este gráfico se muestra la evolución de la pérdida durante la validación del modelo a lo largo de las épocas. También se puede observar una disminución en la pérdida, lo que indica que el modelo es capaz de generalizar correctamente y no está sobreajustando los datos de entrenamiento.

## Contribuciones y Mejoras Futuras

Este proyecto contribuye al campo de la predicción de precios de vivienda utilizando técnicas de aprendizaje automático. Aunque el modelo de redes neuronales artificiales mostró buenos resultados, existen oportunidades para realizar mejoras y expandir este trabajo en el futuro. Algunas posibles mejoras incluyen:

- Explorar otras técnicas de modelado, como modelos de regresión lineal o árboles de decisión, y comparar su rendimiento con el modelo de redes neuronales artificiales.
- Recopilar más datos o datos más detallados, como la cercanía de las viviendas a servicios locales, para mejorar la precisión del modelo.
- Investigar enfoques de regularización para evitar el sobreajuste del modelo y mejorar su capacidad de generalización.

## Licencia

Este proyecto se encuentra bajo la licencia MIT. Puedes consultar el archivo [LICENSE](LICENSE) para más detalles.

