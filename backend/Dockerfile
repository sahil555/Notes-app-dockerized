FROM python:3.8

WORKDIR /backend

COPY ./requirements.txt .

RUN pip3 install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8000
