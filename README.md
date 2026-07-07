# 📦 Automatización - Guías Stock

**Autor:** Kevin Rafael Palomino Ramirez  
**Empresa:** Grucoin S.A.C  
**Proyecto:** Automatización de Gestión de Saldos de Camiones  

---

## 📖 Documentación del Proyecto

### 🎯 Objetivo
Diseñar una solución de automatización que reduzca al mínimo las tareas manuales realizadas diariamente para descargar, procesar, actualizar y distribuir archivos Excel relacionados con los saldos de materiales asignados a camiones desde la plataforma de Luz del Sur.

---

### 🧩 Concepto General
El proyecto busca automatizar un flujo repetitivo que actualmente requiere abrir múltiples archivos, ejecutar macros, copiar y pegar información, actualizar archivos almacenados en OneDrive y enviarlos por correo electrónico.  
La meta es que el usuario solo intervenga cuando sea necesario (ej.: resolver el CAPTCHA de inicio de sesión), mientras el resto del proceso se ejecuta de forma automática.

---

### ⚙️ Herramientas
- **Python** → Automatización web y procesamiento de Excel.  
- **Playwright / Selenium** → Automatización del navegador.  
- **openpyxl / pandas** → Lectura y escritura de Excel.  
- **Microsoft OneDrive** → Almacenamiento.  
- **Microsoft Outlook** → Envío automático de correos.  
- **Power Automate** *(opcional)* → Orquestación e integración con Microsoft 365.  
- **Office Scripts** *(opcional)* → Modificación de archivos directamente en Excel Online.  

---

### 📋 Recursos Necesarios
- Acceso a la plataforma de Luz del Sur.  
- Cuenta corporativa de Outlook.  
- Acceso a OneDrive donde se almacenan los archivos de cada vehículo.  
- Lista de placas en un archivo Excel.  
- Equipo que pueda ejecutar el proceso en segundo plano.  

---

### 🚀 Habilidades que se Desarrollarán
- **Automatización de procesos (RPA).**  
- **Integración entre aplicaciones de Microsoft 365.**  
- **Automatización web.**  
- **Manipulación avanzada de archivos Excel.**  
- **Programación en Python.**  
- **Diseño de flujos de trabajo.**  
- **Reducción de errores mediante automatización.**  

---

### 📌 Alcance
El sistema deberá:
- Descargar la información por cada placa.  
- Transformar los datos que hoy procesa una macro.  
- Actualizar automáticamente el archivo correspondiente de cada vehículo.  
- Guardar o enviar los archivos por correo sin intervención manual adicional.  

---

### ⚠️ Consideraciones
El **CAPTCHA** impide una automatización completa del inicio de sesión.  
La solución contempla que el usuario inicie sesión y resuelva el CAPTCHA una única vez; después de ello el proceso continuará automáticamente.

---

### 🔄 Flujo de la Automatización
1. Leer el Excel con la lista de placas del turno.  
2. Abrir la plataforma de Luz del Sur.  
3. El usuario inicia sesión y resuelve el CAPTCHA.  
4. El sistema navega al módulo de consulta de saldos.  
5. Para cada placa: buscar, filtrar y descargar el archivo Excel.  
6. Procesar automáticamente el archivo descargado (reemplazando la macro).  
7. Identificar el archivo correspondiente en OneDrive (ej.: `AXP-715 - LOS ANDES.xlsx`).  
8. Limpiar el rango de destino y escribir la nueva información.  
9. Guardar el archivo actualizado.  
10. Repetir el proceso para todas las placas.  
11. Al finalizar, mover los archivos a otra carpeta o enviarlos por Outlook con destinatarios, asunto y cuerpo predefinidos.  
12. Generar un registro de ejecución con resultados y posibles errores.  

---

## 📂 Estructura Recomendada del Repositorio
