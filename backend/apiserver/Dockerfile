FROM python:3.8.13-alpine3.16

EXPOSE 8000

# python .pyc 파일 생성하지 않도록 / 로그가 버퍼링없이 즉각 출력되도록
ENV PYTHONDONTWRITEBYTECODE 1 
ENV PYTHONUNBUFFERED 1

ARG FLASK_SECRET_KEY

ENV FLASK_SECRET_KEY $FLASK_SECRET_KEY

# 작업경로 나중에 백엔드 구조 바뀌면 변경할게요
WORKDIR /apiserver
COPY requirements.txt /apiserver/ 


RUN pip install --upgrade pip
RUN pip install -r requirements.txt


COPY . /apiserver/

# CMD ["python"]