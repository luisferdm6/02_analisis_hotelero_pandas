# Hospitality Operations & Revenue Analytics

Pipeline de análisis de datos para auditar la concentración de ingresos por plan de alimentación y categoría hotelera.

### Objetivo del Proyecto
Analizar el desempeño operativo y los patrones de gasto de huéspedes en hoteles urbanos y de resort para identificar los paquetes con mayor impacto en la facturación total.

### Herramientas y Metodología
* **Motor Relacional:** DuckDB y SQL (agrupaciones, filtros condicionales y consultas analíticas).
* **Procesamiento de Datos:** Python y Pandas (limpieza vectorizada de texto a formato numérico decimal `float64`, gestión de tipos categóricos).
* **Visualización Ejecutiva:** Seaborn y Matplotlib (control de márgenes superiores, formateo dinámico de ejes en millones con funciones Lambda y paletas de contraste).

### Aspectos Técnicos Destacados
1. **Limpieza Vectorizada:** Corrección de formatos monetarios (`$`, `,`) directamente sobre columnas completas con métodos vectorizados de texto (`.str.replace`), evitando advertencias de memoria y asegurando tipos de datos listos para análisis matemático.
2. **Formateo No Destructivo:** Implementación de formateadores de eje (`FuncFormatter`) para proyectar cifras en millones (`$M`) en la capa visual, preservando la integridad de las columnas numéricas en la base de datos subyacente.

### Hallazgos Principales
* **Predominio del Bed & Breakfast:** Representa el principal motor de ingresos en ambos tipos de propiedad, superando los $11.3M en hoteles de ciudad.
* **Oportunidad en Resorts:** Las propiedades de resort muestran una mayor adopción proporcional del paquete Half Board (Media Pensión) en comparación con el entorno urbano.
