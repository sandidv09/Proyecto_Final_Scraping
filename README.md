# Proyecto de Web Scraping de Propiedades en República Dominicana

Proyecto académico desarrollado en Python para recopilar, consolidar y analizar información de anuncios inmobiliarios publicados en **Corotos, SuperCasas y Plusval**. El trabajo se ejecuta desde un notebook de Jupyter/Google Colab.

## Contenido del repositorio

- `Proyecto_Final_Scraping.ipynb`: notebook principal con los scrapers, consolidación, limpieza, exportación y reportes.
- `requirements.txt`: dependencias principales para ejecutar el proyecto fuera de Google Colab.
- `.gitignore`: evita subir archivos temporales y resultados generados durante la ejecución.

## Funcionalidades

1. Extracción de anuncios inmobiliarios desde los tres portales.
2. Paginación y límite configurable de registros por portal.
3. Captura de datos como nombre, precio, ubicación, vendedor, tamaño, habitaciones, baños y parqueos, según la información disponible en cada portal.
4. Registro de tiempos y estado de las solicitudes.
5. Consolidación de resultados y eliminación de registros duplicados.
6. Exportación de datos a CSV, Excel, Parquet, JSON y HTML.
7. Generación de un reporte de perfil estadístico y un archivo JSON con el estado de la ejecución.

## Requisitos

- Python 3.10 o superior (recomendado).
- Jupyter Notebook o Google Colab.
- Conexión a Internet para ejecutar la extracción en vivo.

## Instalación local

Desde la carpeta del proyecto, ejecuta:

```bash
python -m pip install -r requirements.txt
```

Luego abre `Proyecto_Final_Scraping.ipynb` en Jupyter Notebook o súbelo a Google Colab y ejecuta las celdas en orden.

> En Google Colab, el notebook instala las dependencias en su primera celda.

## Configuración

En la primera celda de código se encuentran estas variables:

- `EJECUTAR_SCRAPERS_EN_VIVO`: activa o desactiva la extracción en vivo.
- `LIMITE_POR_PORTAL`: establece el máximo de propiedades que se intentan recopilar por portal.
- `CARPETA`: carpeta donde se guardan los resultados generados.

Los resultados se guardan en `resultados_scraping/`. El notebook también genera un archivo ZIP con los resultados al finalizar.

## Consideraciones

- La estructura HTML y los selectores de los portales pueden cambiar; si eso ocurre, será necesario actualizar el scraper correspondiente.
- La disponibilidad de datos depende de lo que cada publicación muestre públicamente. Algunos campos pueden quedar vacíos.
- La extracción puede fallar si un portal limita las solicitudes o requiere mecanismos adicionales de acceso.
- Ejecuta el proyecto de forma responsable, respeta las condiciones de uso de cada sitio y evita realizar solicitudes excesivas.
- Los precios en USD y DOP se identifican por separado; no se convierten automáticamente entre monedas.

## Integrantes

- Lisbeth Salvador - 2025-0736
- Keury Eliezer Rijo Perez - 2025-2137
- Sandi Dotel - 2025-0844
- Carlos Valdez - 2026-1167
- Starlin Michael Castro Arias - 20251334

---

**Proyecto académico de Web Scraping.**
