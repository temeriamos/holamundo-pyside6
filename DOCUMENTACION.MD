
Pasos de solución a los errores al compilar (BUILD):

Paso 1: Verificar la versión y configuración del plugin

    Asegúrate de que el plugin mkdocs-with-pdf esté actualizado a la última versión ejecutando:

    pip install --upgrade mkdocs-with-pdf

    Revisa que tu archivo mkdocs.yml esté correctamente configurado, especialmente las opciones relacionadas con los plugins y el tema.

Paso 2: Instalar el tema necesario

    Si el tema readthedocs no se encuentra, instala el tema mkdocs-material:

    pip install mkdocs-material

Paso 3: Instalar la librería de códigos QR

    Para solucionar el error del filtro qrcode, instala la librería qrcode con el siguiente comando:

    pip install qrcode[pil]

Paso 4: Probar en un entorno limpio

    Si los problemas persisten, prueba crear un entorno virtual limpio e instalar todas las dependencias desde cero:

    python3 -m venv venv
    source venv/bin/activate  # En Linux o macOS
    venv\Scripts\activate  # En Windows

    # Instalar las dependencias
    pip install mkdocs mkdocs-with-pdf qrcode[pil]

Paso 5: Construir el sitio nuevamente

    Una vez realizados los cambios, intenta construir el sitio nuevamente con:

mkdocs build