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

## 📦 4. Instalación de PySide6

Con el entorno virtual activado, instala PySide6:

```bash
pip install PySide6
```

Para verificar que se instaló correctamente, ejecuta:

```bash
python -c "import PySide6; print('Hola Mundo')"
```

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

## 🎯 Resumen
1. **Instalar Python** (`python --version` para verificar).
2. **Instalar `pip`** (`pip --version` para verificar).
3. **Crear y activar un entorno virtual** (`venv`).
4. **Instalar dependencias**.


