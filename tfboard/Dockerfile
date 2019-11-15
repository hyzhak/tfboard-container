ARG PYTHON_VERSION='3.7'

FROM python:${PYTHON_VERSION}

ARG TF_VERSION=2.0.0
ENV TF_VERSION ${TF_VERSION}
ENV PYTHON_VERSION ${PYTHON_VERSION}

# simplified
#
# pip install tensorboard
#
# doesn't work because tensorboard requires tensorflow
# so we should install both

RUN pip install --upgrade pip \
 && pip install --default-timeout=1000 --no-cache-dir tensorflow==${TF_VERSION}

CMD tensorboard --logdir $LOGS_PATH --host 0.0.0.0
