FROM python:latest
COPY requirements.txt /opt/app/
RUN pip3 install -r /opt/app/requirements.txt
COPY app.py /opt/app/
WORKDIR /opt/app/
CMD ["python", "app.py"]
