# 📄 Automatización de Fichas 2.1 y 2.2 (Word) desde Excel

Desarrollado por **Eduard Peñas Balart (UPC - ESEIAAT)**  
Colabora con: **7 Experts**

---

## 🧠 ¿Qué hace este cuaderno?

Este cuaderno de **Google Colab** permite generar de forma automática las fichas de ampliación **2.1 (Personal)** y **2.2 (Entidades y Facturas)** a partir de **archivos Excel**. Estas fichas se exportan en formato Word (.docx) listas para presentar.

---

## 📝 ¿Qué fichas se generan?

- **Ficha 2.1 (Personal)**:  
  Se genera a partir de un único archivo Excel con la información de las personas involucradas en el proyecto (nombre, apellidos, puesto, horas trabajadas, etc.).

- **Ficha 2.2 (Entidades y Facturas)**:  
  Se genera combinando dos archivos Excel:  
  - Uno con información sobre las **entidades colaboradoras**  
  - Otro con las **facturas** asociadas a cada entidad

---

## 📁 Archivos necesarios

Antes de ejecutar el cuaderno, asegúrate de tener en tu Google Drive los siguientes archivos con estos nombres exactos:

- `Excel_Personal_2.1.xlsx`
- `Excel_Colaboraciones_2.2.xlsx`
- `Excel_Facturas_2.2.xlsx`
- `2.1.docx` *(Plantilla Word de la ficha 2.1)*
- `2.2.docx` *(Plantilla Word de la ficha 2.2)*
- `archivo.png`, `Captura1.png`, `Captura2.png` *(Imágenes ilustrativas del proceso)*

---

## ✅ ¿Cómo usar el cuaderno?

1. **Abre el cuaderno en Google Colab**
2. **Ejecuta la primera celda** para instalar dependencias y montar Google Drive.
3. **Sube los archivos Excel y las plantillas Word** a tu Google Drive.
4. **Sigue los pasos numerados en el cuaderno** para generar las fichas automáticamente.
5. **Descarga el archivo Word resultante** desde `/tmp/` o desde el botón de descarga que se generará al final.

---

## 🧪 Requisitos técnicos

- Tener acceso a [Google Colab](https://colab.research.google.com/)
- Conexión con Google Drive
- Archivos Excel rellenados según la plantilla (incluida en el cuaderno)
- Las plantillas `.docx` base deben estar correctamente nombradas y disponibles

---

## 📷 Vista previa

El cuaderno incluye capturas para facilitar la comprensión del proceso paso a paso. También se detallan ejemplos de cómo deben estar rellenadas las tablas Excel.

---

## 💬 Comentarios y soporte

Si tienes sugerencias o detectas errores, no dudes en contactar con el autor o contribuir al repositorio.

---

> Este proyecto tiene fines educativos y administrativos. Uso bajo responsabilidad del usuario.
