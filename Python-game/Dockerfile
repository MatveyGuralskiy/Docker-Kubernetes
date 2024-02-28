#---------Docker file created by Matvey Guralskiy---------
#
#----GitHub profile https://github.com/MatveyGuralskiy----
FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
    libsdl2-dev \
    libsdl2-image-dev \
    libsdl2-ttf-dev \
    ffmpeg \
    libjpeg-dev \  
    libpng-dev \
    libfreetype6-dev \
    libwebp-dev \
    libopenjp2-7-dev \
    zlib1g-dev \
    gcc \
    make \
    libc6-dev
    
RUN apt-get install -y python3 python3-pip

RUN pip3 install pygame

COPY . /app

CMD ["python3", "/app/display_mario.py"]
