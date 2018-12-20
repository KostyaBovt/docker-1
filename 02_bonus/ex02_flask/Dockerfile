FROM python:2-slim

RUN pip install flask

WORKDIR app

RUN echo 'from flask import Flask\napp=Flask(__name__)\n@app.route("/")\ndef hello():\n\treturn "<h1>Hello World !</h1>" ' > /app/hello.py
ENV FLASK_APP=/app/hello.py

EXPOSE 3000

ENTRYPOINT flask run --host=0.0.0.0 --port=3000

# to build
# docker build -t ex02_flask .

# to run
# docker run --rm -d -p 3000:3000 ex02_flask
