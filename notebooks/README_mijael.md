# Notebook Mijael

Este documento contiene un análisis básico en Python usando pandas para trabajar con un archivo Excel de proyectos.

## Archivo
- [mijael.ipynb](mijael.ipynb)

## Qué hace
El notebook realiza lo siguiente:

1. Carga un archivo Excel llamado `plan_de_compras_2025.xlsx`.
2. Muestra una vista previa de los datos con `head()`.
3. Extrae el año a partir del campo `ID Proyecto` utilizando los últimos 2 dígitos.
4. Crea una columna llamada `Año Proyecto`.
5. Filtra los registros correspondientes al año 2025.
6. Muestra el total de registros y la cantidad de proyectos del año 2025.
7. Realiza un conteo de valores a partir de los últimos 4 caracteres del código del proyecto.

## Requisitos
Para ejecutar este notebook se necesita:
- Python
- pandas
- openpyxl (para leer archivos Excel)

## Ejemplo de instalación
```bash
pip install pandas openpyxl
```

## Nota
Asegúrate de que el archivo Excel `plan_de_compras_2025.xlsx` se encuentre en la misma carpeta que el notebook o ajusta la ruta de lectura si está en otra ubicación.
