# ApuntesProyectoFinal
# Análisis de datos de muestra

Para asegurar que la muestra sea representativa de la población, es crucial emplear técnicas adecuadas de muestreo. Entre las opciones existentes, hemos optado por el muestreo por conglomerados. Esta metodología consiste en dividir la población en grupos homogéneos entre sí e internamente heterogéneos (conglomerados). Para entrenar el modelo de aprendizaje automático (ML), se seleccionan una o más de estas unidades y, dentro de ellas, se eligen individuos de manera aleatoria.

En nuestro caso, hemos definido las ciudades como los conglomerados y seleccionaremos las 10 ciudades con más establecimientos que cuenten con reseñas. Este tamaño de muestra representa aproximadamente el 6.31% de la población total.

Para crear la muestra de entrenamiento para el modelo de ML, elegiremos aleatoriamente una cantidad de individuos dentro de las ciudades del estado de New York. Se recomienda un tamaño de muestra de entre 10,000 y 50,000 datos, con la consideración de que estos deben estar balanceados, lo cual no siempre se refleja en la población original.



---

#  Proof of Concept (PoC) para el Producto de Machine Learning

## 1. Objetivo del PoC
El propósito del PoC es evaluar la viabilidad de dos modelos ML:
1. Un modelo que clasifique los comentarios en "positivos" o "negativos" utilizando BERT (Bidirectional Encoder Representations from Transformers).
2. Un modelo adicional que, también utilizando BERT, clasifique los comentarios en "útiles" o "no útiles", con el fin de mejorar la relevancia del contenido presentado a los usuarios.

Además, se busca identificar términos frecuentes en comentarios positivos y negativos para un mejor entendimiento de los patrones lingüísticos, ajustados según filtros específicos que dependen del rubro al que pertenezcan.

## 2. Descripción del Método
Se utilizó el muestreo por conglomerados para garantizar una representación adecuada de la población. Las ciudades fueron definidas como los conglomerados, y se seleccionaron las 10 ciudades con la mayor cantidad de establecimientos con reseñas, representando aproximadamente el 8% de la población total. Posteriormente, se seleccionó aleatoriamente una cantidad de individuos dentro de ciudades del estado de NY, con el objetivo de formar una muestra balanceada para entrenar ambos modelos.

El tamaño sugerido de la muestra varía entre 10,000 y 50,000 datos. Es esencial que esta muestra esté balanceada, aunque este equilibrio no siempre se refleja en la población original.

## 3. Entrenamiento de Modelos con BERT
### Modelo 1: Clasificación de Comentarios en "Positivos" o "Negativos"
- **Preprocesamiento de los Comentarios**: Limpieza y tokenización del texto.
- **Fine-tuning de BERT**: Ajuste del modelo utilizando una muestra etiquetada.
- **Evaluación del Modelo**: Medición del rendimiento con métricas clave.

### Modelo 2: Clasificación de Comentarios en "Útiles" o "No Útiles"
- **Preprocesamiento Similar**: Se utilizaron técnicas de preprocesamiento comparables a las del primer modelo.
- **Fine-tuning de BERT**: Se aplicó BERT nuevamente, ajustando el modelo para distinguir entre comentarios útiles y no útiles.
- **Validación**: Evaluación del rendimiento y generalización a través de técnicas de validación cruzada.

## 4. Identificación de Términos Frecuentes
Además de la clasificación, se realizó un análisis de términos frecuentes en los comentarios positivos y negativos. Este análisis aplica filtros específicos basados en el rubro, para identificar los términos que más afectan la percepción de los usuarios.

- **Extracción y Filtrado de Términos**: Adaptación de los términos según el sector correspondiente.

## 5. Resultados 
### Matriz de Confusión Comentarios Positivos/Negativos

![image](https://github.com/user-attachments/assets/702247fa-6d54-40ac-bb80-b8d106272d0b)


### Matriz de Confusión Comentarios Útiles/No Útiles

![image](https://github.com/user-attachments/assets/2e27b353-857a-4ea2-8692-68914b927daf)


### Recuento de Términos Frecuentes 

![image](https://github.com/user-attachments/assets/eaf811f1-496f-4cc2-b350-2cfe79fcad49)



