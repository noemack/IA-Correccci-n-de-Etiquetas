## 📦 Corrección Inteligente de Etiquetas Dañadas usando Visión Computacional + Machine Learning

Este proyecto simula un caso real donde una **etiqueta dañada** en el equipaje de un aeropuerto debe ser leída y corregida automáticamente usando técnicas de **inteligencia artificial**.

Se combinan dos herramientas clave:
- **Visión por Computadora (OCR con Tesseract)** para leer el texto.
- **Machine Learning (Scikit-learn)** para completar caracteres faltantes en la etiqueta.

---

## 🎯 Objetivo

Demostrar cómo la IA puede ayudar a corregir errores en la lectura de datos visuales, recuperando información faltante en etiquetas mediante predicción.

---

## 🧰 Herramientas

- Python
- OpenCV
- Tesseract OCR
- Scikit-learn
- Pandas
- Numpy

---

## 📦 Instalación

Instalá las librerías necesarias con pip:

```bash
pip install opencv-python pytesseract pandas scikit-learn numpy

```

Debes tener instalado Tesseract OCR:
🔗 https://github.com/tesseract-ocr/tesseract

---

## 🧠 Lógica del proyecto
Se carga una imagen con una etiqueta dañada.

Se extrae el texto con pytesseract (OCR).

Si falta un carácter (representado como _), se aplica un modelo de regresión logística entrenado con ejemplos reales de etiquetas.

El sistema predice el carácter faltante y reconstruye el texto completo.

---

## 📸 Imagen de entrada esperada
Una imagen .jpg con la ruta correspondiente (ajustar en el código):
```bash 
imagen = cv2.imread("C:/.../Python/Imagenes/etiqueta_danada.jpg")
```

---

## 🧪 Entrenamiento del modelo
Se entrena un modelo simple de regresión logística usando etiquetas similares (GBR-120, GBR-121, etc.), utilizando CountVectorizer para representar los datos como caracteres n-grama.

---

## ✅ Resultado esperado

Texto extraído: GBR-12_

Carácter faltante completado automáticamente: 3

Texto final corregido: GBR-123

---

## 🔗 Enlace al Proyecto

[Ver el código completo ](https://github.com/noemack/IA-Correccion-de-Etiquetas/blob/main/Etiquetas.ipynb)
