
# 🧾 Generador automático de fichas Word desde Excel

Este proyecto genera automáticamente un documento Word combinando plantillas `.docx` con datos de personal contenidos en un archivo Excel (`Excel_Personal_2.1.xlsx`). Es útil para informes técnicos, certificaciones y memorias justificativas de proyectos de I+D.

---

## 📁 Estructura del proyecto

```
📦 proyecto/
├── 📄 script.py
├── 📄 funciones.py
├── 📄 Excel_Personal_2.1.xlsx
├── 📄 plantilla_base.docx
├── 📄 Ficha_Ampliacion_Aptdo_2_1_nombre_cliente.docx
└── 📂 output/
```

---

## 🛠 Requisitos

- Python 3.8 o superior
- Google Colab (opcional)
- Librerías necesarias:

```bash
pip install pandas openpyxl python-docx
```

---

## 🔧 Cómo ejecutar el script

1. Asegúrate de que el archivo `Excel_Personal_2.1.xlsx` esté en el mismo directorio o en la ruta indicada.
2. Asegúrate de tener cargada la plantilla Word llamada `2.1.docx` o similar.
3. Ejecuta el script `script.py`, ya sea en local o en Google Colab.
4. Se generará automáticamente el documento Word con todas las fichas combinadas.

---

## 📌 Notas importantes

- Las fechas se formatean automáticamente en el estilo `dd/mm/yyyy`.
- Los valores numéricos en euros se formatean con punto de miles y coma decimal: `1.234,56 €`.
- El campo **Coste horario** muestra el símbolo `€/h` en lugar de `€` para mayor claridad.
- La sección de **"Actividad 3"** se rellena únicamente si hay contenido en las celdas correspondientes.
- Puedes subir tu Excel a Google Drive y montar temporalmente tu unidad si trabajas desde Google Colab.

---

## ☁️ Cómo usarlo como backend en una plataforma

- Extrae la función principal de generación de fichas a un archivo como `generar_fichas.py`.
- Usa la librería `tempfile` para guardar los archivos `.docx` de forma temporal.
- Asegúrate de que el frontend envíe correctamente el archivo `.xlsx`.
- Devuelve el archivo generado en bytes o como descarga desde el backend.
- Usa frameworks como **Flask** o **FastAPI** para hacer accesible el servicio desde HTTP.

---

## 📤 Compartir el proyecto

Para subirlo a GitHub:

1. Crea un repositorio con `git init`.
2. Añade el archivo `README.md` con estas instrucciones.
3. Sube todos los archivos relevantes, excepto ficheros temporales.

---

## 👨‍💻 Indicaciones para otros programadores

- El script debe ejecutarse con un archivo Excel estructurado según el modelo (Nombre, Apellidos, Coste, Horas, etc.).
- Las funciones de estilo están en `funciones.py` (como `formatea_euro`, `formatea_fecha`, etc.).
- El documento Word generado incluye encabezados, tablas, recuadros y saltos de página.
- Si lo adaptas a producción, asegúrate de parametrizar los nombres de entrada/salida y la carga de plantillas.

---

## 📃 Licencia

MIT License. Puedes usarlo, modificarlo y distribuirlo libremente.
