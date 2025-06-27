

# 🧾 API Backend para generación de fichas Word 2.1 y 2.2 desde Excel

Este backend permite generar documentos Word para las fichas de ampliación 2.1 (personal) y 2.2 (entidades y facturas) a partir de archivos Excel. Está preparado para conectarse fácilmente con un frontend en React mediante peticiones HTTP.

---

## ⚙️ Endpoints disponibles

### ▶️ `/generar-ficha-21/`

- **Método**: `POST`
- **Input**: Excel llamado `Excel_Personal_2.1.xlsx` como `multipart/form-data` (campo `excel_file`)
- **Output**: Fichero Word `.docx` con todas las fichas de personal.

### ▶️ `/generar-ficha-22/`

- **Método**: `POST`
- **Input**: Dos archivos Excel:
  - `Excel_Colaboraciones_2.2.xlsx` (campo `colaboraciones`)
  - `Excel_Facturas_2.2.xlsx` (campo `facturas`)
- **Output**: Fichero Word `.docx` con las fichas por entidad y sus costes.

---

## 📁 Estructura recomendada del proyecto

```
/fichas-backend/
├── app.py                 # Servidor FastAPI
├── generar_fichas.py      # Funciones para generar documentos Word
├── plantillas/
│   ├── 2.1.docx           # Plantilla base ficha 2.1
│   └── 2.2.docx           # Plantilla base ficha 2.2
├── output/                # Carpeta de salida para documentos
└── ejemplos/
    ├── Excel_Personal_2.1.xlsx
    ├── Excel_Colaboraciones_2.2.xlsx
    └── Excel_Facturas_2.2.xlsx
```

---

## 🔄 Ejemplo de integración con React

```js
// Subida del Excel 2.1
const formData = new FormData();
formData.append("excel_file", fileInput.files[0]);

fetch("http://localhost:8000/generar-ficha-21/", {
  method: "POST",
  body: formData
})
  .then(res => res.blob())
  .then(blob => {
    const url = window.URL.createObjectURL(blob);
    const a = document.createElement("a");
    a.href = url;
    a.download = "Ficha_Ampliacion_2_1.docx";
    a.click();
  });
```

---

## 📦 Instalación

```bash
pip install fastapi uvicorn python-docx pandas openpyxl
```

---

## ▶️ Cómo ejecutar el backend

```bash
uvicorn app:app --reload
```

---

## ✍️ Notas importantes

- Las plantillas `.docx` deben estar en la carpeta `plantillas/`.
- La salida se guarda automáticamente en `output/`.
- Las funciones están diseñadas para mantener el formato de tablas y estilos definidos en Word.
- La ficha 2.1 puede incluir campos personalizados como actividad 3 y 4.
- La ficha 2.2 genera tablas con desglose de facturas asociadas por entidad.

---

## 📃 Licencia

MIT License – puedes usar, adaptar y distribuir libremente este backend.
