# Minería de Reglas de Asociación - Predicción de Selección de Pasantías

Este repositorio contiene la definición y solución de un problema de minería de reglas de asociación utilizando el conjunto de datos de predicción de selección de pasantías (*Internship Selection Prediction Dataset*).

## Integrantes del Equipo
* **Marcelo Rebolledo**
* **Sebastián Bustos**
* **Esteban Massa**
* **Francisco Sanhueza**

---

## Pregunta Guía
El análisis y modelo desarrollado en este proyecto busca responder de manera directa a la siguiente pregunta:
> **¿Qué perfil académico y técnico maximiza la probabilidad de obtener una práctica profesional?**

---

## Descripción del Proyecto
El dataset original está diseñado para modelar y predecir si un estudiante será seleccionado para una pasantía (problema de clasificación binaria) a partir de 21 características que abarcan aspectos académicos, habilidades técnicas, experiencia en proyectos y rasgos conductuales.

Para aplicar reglas de asociación, el flujo del proyecto implementado en [reglas_asociacion_proyecto.ipynb](reglas_asociacion_proyecto.ipynb) realiza lo siguiente:
1. **Simulación del Dataset**: Generación controlada de un conjunto de datos sintético de 10,000 registros para replicar el esquema y correlaciones reales descritos en el conjunto original de Kaggle.
2. **Discretización y Preprocesamiento**: Transformación de las variables numéricas continuas y discretas en variables booleanas/ítems transaccionales (por ejemplo, clasificar la nota promedio `CGPA` en rangos alto/medio/bajo, o la cantidad de proyectos en con/sin experiencia).
3. **Minería con Apriori Manual**: Implementación desde cero en Python estándar (siguiendo las metodologías paso a paso de los tutoriales del curso) para la obtención de itemsets frecuentes.
4. **Generación de Reglas de Asociación**: Evaluación y filtrado de reglas basadas en soporte, confianza y lift.
5. **Análisis del Perfil**: Filtrado de reglas que tienen como consecuente `{Seleccionado}` (es decir, el éxito en obtener la práctica) y antecedentes que corresponden únicamente a características académicas y técnicas, respondiendo directamente a la pregunta guía.

## Cómo Ejecutar
1. Clonar el repositorio.
2. Abrir Jupyter Notebook o Jupyter Lab en este directorio.
3. Ejecutar todas las celdas de [reglas_asociacion_proyecto.ipynb](reglas_asociacion_proyecto.ipynb).
   * El notebook generará automáticamente el archivo de datos `Internship_Selection_Dataset.csv` y correrá el flujo de preprocesamiento, modelado e interpretación.
