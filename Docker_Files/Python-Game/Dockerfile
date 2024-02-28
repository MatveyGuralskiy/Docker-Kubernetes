#---------Docker file created by Matvey Guralskiy---------
#
#----GitHub profile https://github.com/MatveyGuralskiy----

FROM python:3.12.2-alpine3.18

RUN apt-get update && apt-get install -y \
    libsdl-dev \
    libsdl-image1.2-dev \
    libsdl-ttf2.0-dev \
    libavformat-dev \
    libswscale-dev

COPY /DISPLAY_MARIO/requirements.txt /app/requirements.txt
WORKDIR /app
RUN pip install --no-cache-dir -r requirements.txt

COPY . /app

CMD ["python", "DISPLAY_MARIO.py"]