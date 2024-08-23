FROM python:latest
WORKDIR /usr/src/app
RUN groupadd -g 1100 app_user && \
    useradd -m -s /bin/bash -u 1100 -g 1100 app_user
RUN chown -R app_user:app_user /usr/src/app
USER app_user
COPY ./requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt