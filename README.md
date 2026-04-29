# Proyecto-EDA---ThePower
Este proyecto tiene como objetivo realizar un Análisis Exploratorio de Datos (EDA) sobre el catálogo global de Netflix, utilizando exclusivamente Microsoft Excel como herramienta de procesamiento y visualización.

El análisis se centra en identificar patrones de producción de contenido, tendencias temporales, distribución geográfica y preferencias de género por país. El dataset utilizado contiene información de 8,789 títulos disponibles en la plataforma, extraído del repositorio público de Kaggle.

**Objetivos específicos:**
- Realizar limpieza y transformación de datos para garantizar la calidad del análisis
- Analizar la distribución del contenido por tipo (películas vs. series)
- Identificar tendencias de producción por año de lanzamiento
- Explorar la distribución geográfica del contenido producido
- Analizar los géneros más representados por país de origen
- Desarrollar un dashboard interactivo para la visualización de resultados


## 🛠️ Requisitos Técnicos

**Software necesario:**
- Microsoft Excel 2016 o superior (desarrollado en Excel 365)
- Sistema operativo: Windows, macOS o Linux con compatibilidad Office

**Dataset:**
- Fuente: [Netflix Shows - Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)
- Archivo: `netflix_titles.csv`
- Licencia: CC0: Public Domain

**Conocimientos recomendados:**
- Manejo intermedio de Excel (tablas dinámicas, funciones de texto, formato condicional)
- Conceptos básicos de análisis exploratorio de datos

## 📊 Metodología y Proceso de Limpieza

### 1. Diagnóstico Inicial de Calidad de Datos
Se realizó un análisis preliminar para identificar:
- Valores nulos por columna (especialmente en `director` ~30% y `country` ~9%)
- Formatos inconsistentes en fechas y texto
- Campos con múltiples valores separados por comas

### 2. Transformaciones Aplicadas

| Columna | Transformación | Herramienta/Fórmula |
|---------|---------------|-------------------|
| `country` | Extracción del primer país | Relleno Rápido (Ctrl+E) |
| `listed_in` | Extracción del género principal | Relleno Rápido (Ctrl+E) |
| `date_added` | Conversión a formato fecha | FECHAVAL() |
| `title`, `description` | Eliminación de espacios redundantes | ESPACIOS() |
| Valores vacíos | Imputación con "Desconocido" | Función SI.ERROR() |

### 3. Herramientas de Excel Utilizadas
- Tablas dinámicas para agregación y segmentación de datos
- Segmentadores (Slicers) para interactividad en el dashboard
- Formato condicional para visualización de patrones (heatmaps)
- Gráficos dinámicos para representación visual de tendencias

## 📈 Resultados Principales

### Distribución del Contenido
| Métrica | Valor | Porcentaje |
|---------|-------|-----------|
| Total de títulos | 8,789 | 100% |
| Películas (Movies) | 6,125 | 69.7% |
| Series (TV Shows) | 2,664 | 30.3% |

### Evolución Temporal
- El crecimiento de contenido añadido a Netflix muestra un pico máximo en **2018**
- A partir de 2019 se observa una estabilización, posiblemente relacionada con cambios estratégicos en la adquisición de contenido

### Distribución Geográfica (Top 5)
| País | Cantidad de títulos | % del total |
|------|-------------------|-------------|
| United States | 3,140 | 35.7% |
| India | 980 | 11.2% |
| United Kingdom | 622 | 7.1% |
| Japan | 415 | 4.7% |
| Canada | 389 | 4.4% |

### Géneros por País (Hallazgos Destacados)
- **India**: Predominio de Dramas internacionales (398 títulos)
- **Japón**: Especialización en Action & Adventure (47 títulos)
- **Reino Unido**: Fuerte presencia de Documentales (102 títulos)
- **Estados Unidos**: Catálogo diversificado con presencia equilibrada en múltiples géneros

## 💡 Uso del Dashboard

1. Abrir el archivo `Proyecto EDA - Adela Labrador - Datos Netflix.xlsx`
2. Navegar a la hoja **Dashboard**
3. Utilizar los segmentadores ubicados en la parte superior para filtrar por:
   - Tipo de contenido (Movie / TV Show)
   - País de producción
   - Año de lanzamiento
4. Los gráficos y KPIs se actualizarán automáticamente según los filtros seleccionados

## 🔍 Conclusiones

- Netflix mantiene un catálogo predominantemente cinematográfico (70% películas)
- Estados Unidos concentra más de un tercio del contenido global, reflejando su rol como mercado principal
- Existe una clara especialización de géneros por región, lo que sugiere estrategias de contenido localizadas
- El dashboard desarrollado permite una exploración interactiva eficiente sin necesidad de herramientas de programación

## 🔄 Próximos Pasos

Posibles líneas de expansión para este análisis:
- Incorporar análisis de sentimiento sobre las descripciones de contenido
- Cruzar datos de ratings con año de lanzamiento para estudiar evolución de clasificaciones por edades
- Integrar datos externos (ej. IMDb) para enriquecer el análisis con puntuaciones de audiencia
- Migrar el proceso a Python/R para automatizar la limpieza y permitir escalabilidad

## ✒ Autor

**Adela Labrador**  
🎓 Máster en Data Analytics - ThePower  
📧 adelalabrador22@gmail.com  
🔗 [GitHub](https://github.com/adelalabrador22-sudo)  

*Fecha de entrega: Abril 2026*
