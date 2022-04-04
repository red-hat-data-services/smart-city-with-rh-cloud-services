FROM registry.access.redhat.com/ubi8/python-38:latest

USER 0

COPY ./requirements.txt requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

COPY ./app.py app.py

ENV PYTHONPATH=/opt/app-root/src

USER 1001

CMD ["python","/opt/app-root/src/app.py"]
