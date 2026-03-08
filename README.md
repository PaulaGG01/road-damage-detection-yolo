# Detección de daños en pavimentos con YOLOv11

## Descripción del proyecto
Este proyecto implementa un modelo de visión computacional para detectar daños en pavimentos utilizando técnicas de inteligencia artificial. El objetivo es demostrar un flujo completo de desarrollo de un modelo de detección de objetos aplicado al ámbito de infraestructura urbana.

El modelo fue entrenado utilizando la arquitectura YOLOv11 para identificar zonas de deterioro en imágenes de pavimentos.

---

## Dataset
El dataset fue creado utilizando la plataforma Roboflow y contiene **149 imágenes anotadas** de pavimentos con presencia de daños.

Las imágenes se dividieron en:

- 80% entrenamiento  
- 10% validación  
- 10% prueba  

Además, se aplicaron técnicas de **data augmentation** para mejorar la capacidad de generalización del modelo.

---

## Modelo utilizado
Se utilizó el modelo **YOLOv11 Object Detection (Fast)** entrenado a través de Roboflow.

---

## Resultados del modelo

Métricas obtenidas en el conjunto de validación:

- **mAP@50:** 25.4%
- **Precisión:** 45.1%
- **Recall:** 31.4%

El modelo logra identificar zonas de daño en pavimentos, aunque su rendimiento está limitado por el tamaño reducido del dataset.

---

## Evaluación del modelo

Durante la inferencia se analizó el comportamiento del modelo modificando el **confidence threshold**.

- Con un threshold de **50%**, el modelo detecta daño con una confianza aproximada de **78%**.
- Con **70%**, la detección se mantiene visible.
- Con **80%**, la detección desaparece, ya que la confianza del modelo es inferior al nuevo umbral.

Esto demuestra cómo el parámetro de confianza permite controlar el equilibrio entre detecciones y falsos positivos.

---

## Posibles mejoras

Para mejorar el rendimiento del modelo se podrían aplicar las siguientes estrategias:

- aumentar el tamaño del dataset
- incorporar ejemplos negativos (pavimentos sin daño)
- diferenciar distintos tipos de deterioro
- optimizar hiperparámetros del modelo

---

## Aplicación en ciudades inteligentes

Este tipo de modelos podría ser utilizado por municipalidades o entidades de infraestructura para detectar automáticamente daños en pavimentos a partir de imágenes capturadas por vehículos de inspección o cámaras urbanas, permitiendo priorizar intervenciones de mantenimiento.
