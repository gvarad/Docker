FROM python:3.8

LABEL "app" = "FlaskApp"

COPY . .

RUN pip install -r requirements.txt

EXPOSE 5000

CMD ["flask" , "run" , "--host" , "0.0.0.0"]

