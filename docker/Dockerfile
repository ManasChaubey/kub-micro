FROM ubuntu:latest

RUN apt update

RUN apt install -y python3 python3-pip 

COPY ./main.py /

COPY ./requirements.txt /

RUN python3 -m pip install -r requirements.txt

CMD ["uvicorn", "--host=0.0.0.0", "--port=80", "main:app"]