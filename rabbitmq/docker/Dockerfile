FROM rabbitmq:3-management

ARG UID=1000
RUN adduser --uid ${UID} --disabled-password --gecos "" appuser && \
    mkdir -p /home/appuser/.ssh && \
    echo "StrictHostKeyChecking no" >> /home/appuser/.ssh/config && \
    chown -R appuser:appuser /home/appuser

RUN apt-get update && apt-get install -y vim

USER ${UID}