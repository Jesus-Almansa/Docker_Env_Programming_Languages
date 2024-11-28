# Usa la imagen base que prefieras
FROM python:3.12-slim-bookworm

# Establece el directorio de trabajo
WORKDIR /usr/src/app/workspace

# Actualiza los paquetes e instala Git y las dependencias necesarias para cv2
RUN apt-get update && apt-get install -y --no-install-recommends \
    git \
    curl \
    sudo \
    nano \
    build-essential \
    libgl1-mesa-glx \
    libglib2.0-0 \
    libtesseract-dev \
    tesseract-ocr \
    tesseract-ocr-eng \
    wget \
    unzip && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

# Instala las bibliotecas de Python que necesitas
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Crea el usuario 'JESUS' y 'MARCUS', utilizando las variables de entorno para las contraseñas
ARG JESUS_PASSWORD
ARG MARCUS_PASSWORD
RUN useradd -ms /bin/bash jesus && \
    echo "jesus:${JESUS_PASSWORD}" | chpasswd && \
    usermod -aG sudo jesus && \
    useradd -ms /bin/bash marcus && \
    echo "marcus:${MARCUS_PASSWORD}" | chpasswd && \
    usermod -aG sudo marcus

# Configura que JESUS y MARCUS puedan usar sudo sin contraseña
RUN echo "jesus ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers && \
    echo "marcus ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers && visudo -c

# Cambia la propiedad de todos los archivos y directorios de /usr/src/app/workspace a JESUS y MARCUS
RUN chown -R jesus:jesus /usr/src/app/workspace && \
    chown -R marcus:marcus /usr/src/app/workspace

# Establece el usuario JESUS como el usuario por defecto
USER jesus

# Comando por defecto cuando inicie el contenedor
CMD ["bash", "-c", "cd /usr/src/app/workspace && bash"]
