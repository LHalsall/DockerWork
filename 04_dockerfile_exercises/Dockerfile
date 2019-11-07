ARG PYTHON_VERSION=2.7.15
FROM python:${PYTHON_VERSION}
WORKDIR /opt/python-server
COPY ./python-server-${PYTHON_VERSION}.py app.py
COPY index.html .
RUN sed -i "s/{{PYTHON_VERSION}}/${PYTHON_VERSION}/g" index.html
EXPOSE 9000
ENTRYPOINT ["/usr/local/bin/python", "app.py"]
