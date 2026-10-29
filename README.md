# Brecha digital y educación en el Perú 2025

Anthony Kelman Mamani Vargas — Ingeniería de Sistemas, ciclo VIII.
Docente: Angel Rosendo Condori Coaquira. Universidad Peruana Unión.

## Una sola entrega
- Proyecto_Brecha_Digital.ipynb: único notebook Jupyter, con todo el código y las salidas de sus 19 celdas ejecutadas. Incluye limpieza, integración, EDA general y por edad, clustering, cuatro clasificadores, validación por conglomerado, SHAP, exportación de todas las bases utilizadas y evidencias.
- Informe.docx: único informe, editable en Word. El índice de secciones está visible después de la portada, con enlaces internos. No se adjunta PDF.
- data_limpia/: bases ENAHO 100, 200, 300 y Sumaria del corte 2025 y variables utilizadas; servicios ESCALE, contexto distrital, base integrada de 17 807 estudiantes, particiones, diccionario e inventario. Consultar LEEME.md para su alcance y tratamiento de faltantes.
- evidencias/: figuras, tablas, auditorías, logo utilizado y registros.
- requirements.txt y .gitignore: apoyo de reproducción y publicación del mismo notebook en GitHub.

## GitHub
Se usa este mismo Proyecto_Brecha_Digital.ipynb; no hay un segundo notebook ni código diferente para GitHub. Puede acompañarse con README.md, requirements.txt y .gitignore. La carpeta de microdatos queda excluida por .gitignore. No se ha publicado un repositorio.

## Ejecutar de nuevo
1. Instalar Python 3.12 y las dependencias de requirements.txt en el entorno de Jupyter.
2. Descomprimir los ZIP originales INEI y MINEDU, incluidos sus ZIP internos, y colocar los CSV y DBF del proyecto dentro de data_cruda/ (pueden mantenerse subcarpetas). Alternativamente, definir PROYECTO_RAW con la ubicación de los originales ya extraídos.
3. Abrir este único notebook desde la carpeta de entrega y ejecutar las celdas en orden. Todos los procedimientos están dentro del notebook; no requiere scripts .py externos.
4. La ejecución genera data_limpia/ y evidencias/. La ejecución entregada utilizó una caché opcional de columnas 2025 obtenidas de los originales; la ruta está documentada en la salida. Sin PROYECTO_CACHE, las funciones leen los archivos crudos.

Los ZIP originales voluminosos no se duplican en la entrega. Las bases limpias conservan las ausencias válidas; los predictores se imputan dentro del entrenamiento, no sobre la etiqueta. Las estimaciones son transversales y no prueban causalidad. El detalle del alcance y las limitaciones se encuentra en el informe.

## Correspondencia del EDA entre informe y notebook
El capítulo 3 y los anexos O a S desarrollan el EDA: inventario del material, dimensiones y claves por fuente, faltantes por variable, distribuciones, frecuencias categóricas, señales IQR, balance de la etiqueta y correlaciones. Los archivos adicionales de salud 400, empleo 500 y Sumaria 12g se revisan en sus campos comunes del corte 2025; no se afirma un análisis exhaustivo de sus preguntas sustantivas ni se usan en los modelos. Las tablas completas y los gráficos se generan en el mismo notebook y están en evidencias/.
