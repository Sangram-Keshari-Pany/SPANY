FROM python:3.12-slim
WORKDIR /app
COPY ./SPANY ./ 
COPY ./SPANY/requirements.txt ./ 

RUN pip install --upgrade pip --no-cache-dir
RUN pip install -r /app/requirements.txt --no-cache-dir


EXPOSE 8000

# CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
CMD ["gunicorn", "SPANY.wsgi:application", "--bind", "0.0.0.0:8000"]
