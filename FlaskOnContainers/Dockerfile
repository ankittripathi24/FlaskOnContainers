FROM ubuntu:22.04
MAINTAINER ankittripathi2402@gmail.com

RUN apt-get update -y
RUN apt-get install gunicorn -y

COPY flaskapp/requirements.txt requirements.txt
COPY flaskapp /opt/

RUN pip install -r requirements.txt
WORKDIR /opt/

CMD ["gunicorn","-b","0.0.0.0:8000","app:app","--workers=5"]



