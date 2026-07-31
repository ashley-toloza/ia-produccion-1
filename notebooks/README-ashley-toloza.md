# 📊 Análisis de Plan de Compras 2025 (MINVU)

🎯 **Objetivo del Proyecto**

El propósito de este proyecto es realizar un Análisis Exploratorio de Datos (EDA) detallado y estructurado sobre la Planilla de Compras 2025 del Ministerio de Vivienda y Urbanismo (MINVU). El objetivo final es identificar y cuantificar los patrones de programación, montos comprometidos, distribución por unidades de compra y plazos temporales, sirviendo como base estratégica para la gestión y control presupuestario.

🔑 **Análisis y Hallazgos Clave**

El análisis se centró en un riguroso proceso de carga, limpieza de tipos de datos, análisis de valores nulos, inspección temporal de las fechas de inicio, análisis de distribución y procesamiento de IDs para el filtrado por año y códigos de proyectos.

💡 **Conclusión Ejecutiva**

Basado en la evaluación integral de los registros de compras, se observa una fuerte concentración en proyectos de carácter operacional y estratégico distribuidos a lo largo del territorio nacional, destacando la SEREMI MINVU V Región y el nivel central como los principales actores en volumen de requerimientos. El control de las fechas de inicio, los montos de arrastre y la segmentación temporal por año son críticos para la correcta ejecución presupuestaria anual.

📈 **Métricas y Análisis Clave**

- **Volumen Total:** Análisis de un total de 831 registros de compras correspondientes al periodo evaluado.
- **Distribución por Unidad de Compra:** Identificación de las distintas SEREMIs y servicios involucrados, evidenciando un alto volumen de gestión en la V Región y en el Nivel Central.
- **Análisis Temporal:** Evaluación del rango de fechas de inicio de compra (desde 2022 hasta proyecciones en 2026), extracción de años a partir del `ID Proyecto`, filtrado específico del periodo 2025 y cálculo de la diferencia en días respecto a la publicación del PAC 2025.
- **Montos y Arrastres:** Cuantificación de los montos totales de los ítems, análisis de los ítems de arrastre incorporados para la planificación financiera y conteo de valores basados en los códigos de proyecto.

📊 **Visualizaciones Clave**

Se generaron gráficos esenciales para validar y comunicar los insights más fuertes:
- **Gráfico de Barras Horizontales:** Muestra la cantidad de registros por Unidad de Compra, facilitando la identificación rápida de las dependencias con mayor carga operativa.
- **Gráfico de Tendencia Temporal:** Visualiza la cantidad de compras iniciadas por mes y año para detectar estacionalidades o concentraciones presupuestarias.

💻 **Estructura y Tecnologías**

El proyecto se desarrolló siguiendo un flujo modular organizado en la carpeta `notebooks/`:
- **Consolidación y Carga / EDA (Ashley Toloza):** Ingesta del archivo Excel, inspección de nulos, resúmenes estadísticos (`describe()`), validación de rangos, previsualización y análisis temporal/de fechas.
- **Tablas, Gráficos de Resumen y Procesamiento (Felipe Vallejos):** Generación de tablas agrupadas, visualizaciones con Matplotlib, conteos de valores y extracción de año desde el `ID Proyecto`.
- **Procesamiento y Filtros (Mijael):** Carga del archivo Excel, vista previa (`head()`), extracción del año desde el `ID Proyecto` (últimos 2 dígitos), filtrado del año 2025, conteo de registros y análisis de los últimos caracteres del código de proyecto.
- **Análisis y Filtrado Básico (Pablo Villegas - Rama: `Villegates`):** Carga del archivo Excel (`plan_de_compras_2025.xlsx`), vista previa, extracción y creación de la columna `Año Proyecto`, filtrado del año 2025 y conteo a partir de los códigos de proyecto.

### Tecnologías Utilizadas
- **Python:** Lenguaje principal de análisis.
- **Pandas / NumPy:** Para la manipulación, limpieza, transformación y agregación de datos.
- **Matplotlib:** Para la generación de gráficos de resumen y análisis temporal.
- **openpyxl:** Librería requerida para la lectura de archivos Excel.

📁 **Contenido del Repositorio**

- `notebooks/ashley-toloza.ipynb`: Notebook de Ashley dedicado a la carga de datos, inspección inicial (EDA) y análisis de fechas.
- `notebooks/felipe-vallejos.ipynb`: Notebook de Felipe que agrupa las tablas de resumen, los gráficos estadísticos y el análisis de distribución por Unidad de Compra.
- `notebooks/mijael.ipynb`: Notebook complementario de Mijael enfocado en la vista previa (`head()`), extracción del año desde el `ID Proyecto`, filtrado del año 2025 y conteo de códigos.
- `notebooks/Villegates.ipynb`: Notebook de Pablo Villegas centrado en el análisis básico, extracción del año desde el `ID Proyecto`, filtrado de registros 2025 y conteo de valores de códigos de proyecto.
- `plan_de_compras_2025.xlsx`: Archivo de datos fuente de compras públicas.
- `README.md`: Documento actual que presenta la estructura, hallazgos clave y descripción del proyecto.

⚙️ **Requisitos e Instalación**

Para ejecutar los notebooks de este repositorio se necesita:
- Python
- pandas
- openpyxl

Ejemplo de instalación:
```bash
pip install pandas openpyxl
```

> **Nota:** Asegúrate de que el archivo Excel `plan_de_compras_2025.xlsx` se encuentre en la ubicación correcta respecto a los notebooks (ajustando las rutas relativas como `../plan_de_compras_2025.xlsx` según corresponda).

✨ **Posibles Mejoras (Adicionales)**

- **Automatización de Reportes:** Implementar scripts ejecutables para actualizar automáticamente los tableros de control ante nuevas versiones del PAC.
- **Modelado Predictivo:** Incorporar análisis de plazos para estimar retrasos entre la publicación del PAC y el inicio efectivo de las contrataciones.