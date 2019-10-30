FROM python:3
ENV PYTHONUNBUFFERED 1
RUN apt-get update && \
    apt-get install -y build-essential python3-dev \
    libldap2-dev libsasl2-dev ldap-utils tox \
    lcov valgrind
RUN mkdir /code
WORKDIR /code
COPY requirements.txt /code/
RUN pip install -r requirements.txt
COPY . /code/
