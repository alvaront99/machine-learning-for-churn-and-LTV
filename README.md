# Estrategia de Optimización de LTV: Predicción de Churn 

## Resumen del Proyecto
Este proyecto aborda uno de los retos más críticos en el sector de telecomunicaciones: la tasa de abandono de clientes (**Churn Rate**). El objetivo fue desarrollar un modelo predictivo capaz de identificar patrones de comportamiento predecibles en clientes, permitiendo a la empresa pasar de una estrategia reactiva a una **anticipativa**.

> **Nota:** Este proyecto refleja mi enfoque analítico profesional. A pesar de haber alcanzado una exactitud del 81% en el modelo, considero esta versión como un paso intermedio. El despliegue a producción requiere un mayor refinamiento para asegurar que las campañas de fidelización sean rentables y efectivas.

## Ciclo de Vida del Modelo 

1. **Comprensión de Negocio:** Análisis del impacto del Churn en el *Lifetime Value* (LTV) del cliente y la importancia de la retención sobre la captación.
2. **Procesamiento de Datos:** Limpieza y estructuración del dataset para identificar variables clave relacionadas con la estabilidad contractual y la antigüedad.
3. **Modelado (Regresión Logística):** Selección de un modelo de regresión logística por su interpretabilidad y equilibrio en el rendimiento, logrando un **81% de exactitud**.
4. **Validación:** Evaluación mediante precisión y *recall* para asegurar que las inversiones en fidelización se dirijan a los perfiles correctos.

## Diagrama 

```mermaid
graph LR
    subgraph "Entrada"
        Data[Dataset: Telco Churn]
    end

    subgraph "Procesamiento"
        Prep[Limpieza / Feature Engineering]
    end

    subgraph "Modelado"
        Model[Regresión Logística]
    end

    subgraph "Evaluación"
        Metrics[Exactitud 81% / Precisión 68%]
    end

    subgraph "Decisión Estratégica"
        Final{¿Producción?}
    end

    Data --> Prep
    Prep --> Model
    Model --> Metrics
    Metrics --> Final
    Final -- "En fase de afinado" --> Monitor[Monitorización / Mejora continua]

    style Model fill:#f96,stroke:#333,color:black
    style Final fill:#ff9,stroke:#333,color:black
```

## Stack Tecnológico
* **Lenguaje:** Python (Pandas, Scikit-Learn).
* **Algoritmo:** Regresión Logística.
* **Técnicas:** Análisis de correlación, validación de modelos, métricas de clasificación.

## Reflexión Crítica: ¿Por qué no está en producción?
Como analista enfocado en resultados de negocio, aplico un criterio estricto antes de pasar una solución a entornos de producción:

* **Precisión vs. Impacto Económico:** Aunque el modelo es preciso (68%) en la detección de clientes en riesgo, reconozco que aún hay margen de mejora para minimizar falsos positivos. En el sector Telco, una campaña de fidelización errónea puede costar más que el riesgo mismo.
* **Camino a la madurez:** El modelo está en fase de "afinado". Mi objetivo es seguir iterando sobre el dataset para aumentar la sensibilidad del modelo antes de que el equipo de marketing base sus presupuestos en esta herramienta.

## Valor Estratégico
* **Optimización de Recursos:** Identificación precisa de segmentos en riesgo para dirigir esfuerzos de fidelización.
* **Estabilidad Económica:** Preservación de la *customer base* y mejora directa en la estabilidad a largo plazo de la compañía.
* **Cultura Data-Driven:** Este trabajo demuestra que el Machine Learning no es un evento aleatorio, sino una herramienta para liderar el mercado mediante la anticipación.

## Documentación
La memoria detallada con el análisis comparativo, las métricas y la estrategia de negocio se encuentra en [Memoria_TFG.pdf](https://github.com/alvaront99/machine-learning-for-churn-and-LTV/blob/main/Memoria-ML-churn.pdf).
