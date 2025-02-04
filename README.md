# 📌 Guía para instalar y configurar Python correctamente

Voy a explicarte paso a paso, sin cosas técnicas complicadas, cómo hacer que Python funcione bien en tu computadora, instalar dependencias y ejecutar una aplicación.

---

## 🖥 1. Instalación de Python 3

Python es el lenguaje que necesitas para programar y ejecutar aplicaciones.

### 🔹 Windows
1. **Descargar Python**
   - Ve a [la página oficial de Python](https://www.python.org/downloads/) y descarga la última versión de Python 3.
   - Asegúrate de que sea la versión para **Windows** (archivo `.exe`).

2. **Instalar Python**
   - Abre el archivo `.exe` descargado.
   - Marca la opción **"Add Python to PATH"** (esto es importante).
   - Haz clic en **"Install Now"** y espera a que termine.
   - Para comprobar que todo salió bien, abre la terminal (`cmd`) y escribe:
     ```sh
     python --version
     ```
     o  
     ```sh
     py --version
     ```
     Debe mostrar algo como `Python 3.x.x`.

### 🔹 Ubuntu
1. **Actualizar el sistema** (opcional, pero recomendable):  
   ```sh
   sudo apt update && sudo apt upgrade -y
   ```
2. **Instalar Python** (si no lo tienes):  
   ```sh
   sudo apt install python3 -y
   ```
3. **Verificar la instalación**  
   ```sh
   python3 --version
   ```
   Debe mostrar algo como `Python 3.x.x`.

---

## 🛠 2. Instalación y activación de pip

`pip` es el administrador de paquetes de Python.

### 🔹 Windows
- Si instalaste Python correctamente, `pip` ya está incluido. Verifica con:
  ```sh
  pip --version
  ```
  Si no funciona, intenta con:
  ```sh
  py -m pip --version
  ```
  Si no está instalado, ejecútelo manualmente con:
  ```sh
  python -m ensurepip --default-pip
  ```
  Luego actualízalo:
  ```sh
  python -m pip install --upgrade pip
  ```

### 🔹 Ubuntu
- Para asegurarte de que `pip` está instalado, usa:
  ```sh
  sudo apt install python3-pip -y
  ```
- Verifica que funciona:
  ```sh
  pip3 --version
  ```
- Actualízalo:
  ```sh
  pip3 install --upgrade pip
  ```

---

## 🔄 3. Creación y activación del entorno virtual

Un **entorno virtual** es como una caja aislada donde puedes instalar librerías sin afectar el sistema.

### 🔹 Windows
1. **Crear un entorno virtual**  
   ```sh
   python -m venv mi_entorno
   ```
2. **Activar el entorno virtual**  
   ```sh
   mi_entorno\Scripts\activate
   ```
   - Si ves `(mi_entorno)` al inicio de la línea de comandos, ¡ya está activado!

### 🔹 Ubuntu
1. **Instalar `venv` (si no lo tienes)**  
   ```sh
   sudo apt install python3-venv -y
   ```
2. **Crear el entorno virtual**  
   ```sh
   python3 -m venv mi_entorno
   ```
3. **Activar el entorno virtual**  
   ```sh
   source mi_entorno/bin/activate
   ```
   - Si ves `(mi_entorno)` al inicio de la línea, significa que está activado.

---

## 📦 4. Instalación de dependencias

1. Asegúrate de que el **entorno virtual está activado**.
2. Instala las librerías desde un archivo `requirements.txt` con:
   ```sh
   pip install -r requirements.txt
   ```
3. Si no tienes el archivo `requirements.txt`, instala las librerías manualmente:
   ```sh
   pip install flask django requests
   ```
4. Verifica que están instaladas:
   ```sh
   pip list
   ```

---

## 🚀 5. Ejecución de la aplicación

1. **Asegúrate de que el entorno virtual está activado**.
2. Ejecuta tu aplicación:
   ```sh
   python app.py
   ```
3. Si usas `Flask`:
   ```sh
   flask run
   ```
4. Si usas `Django`:
   ```sh
   python manage.py runserver
   ```
5. Abre en el navegador `http://127.0.0.1:5000` o `http://127.0.0.1:8000`.

---

## 🛑 Para desactivar el entorno virtual

- **Windows**:
  ```sh
  deactivate
  ```
- **Ubuntu**:
  ```sh
  deactivate
  ```

---

## 🎯 Resumen rápido
1. **Instalar Python** (`python --version` para verificar).
2. **Instalar `pip`** (`pip --version` para verificar).
3. **Crear y activar un entorno virtual** (`venv`).
4. **Instalar dependencias** (`pip install -r requirements.txt`).
5. **Ejecutar la aplicación** (`python app.py` o `flask run`).

Con esto ya puedes trabajar con Python de forma limpia y organizada en Windows o Ubuntu. 🚀

