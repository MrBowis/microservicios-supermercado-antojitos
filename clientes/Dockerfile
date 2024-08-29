# Usa una imagen base de Python 3.x
FROM python:3.11-slim

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia el archivo de requerimientos al directorio de trabajo
COPY requirements.txt /app/

# Instala las dependencias
RUN pip install --no-cache-dir -r requirements.txt

# Copia todo el proyecto al directorio de trabajo
COPY . /app/

# Expone el puerto 8000, que es el puerto por defecto de Django
EXPOSE 8000

# Especifica el comando que se ejecutará cuando se inicie el contenedor
CMD ["python", "app/manage.py", "runserver"]
