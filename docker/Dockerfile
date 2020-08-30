FROM alpine:latest

ENV WORKSPACE=/mnt

RUN apk upgrade --available \
    && apk add -U --no-cache build-base curl libffi-dev openssl-dev \
    libxml2-dev libxslt-dev openssh python3 python3-dev \
    && curl https://bootstrap.pypa.io/get-pip.py -o /tmp/get-pip.py \
    && python3 /tmp/get-pip.py \
    && pip install ansible boto3 botocore \
    && mkdir -p /usr/share/ansible/plugins/modules \
    && rm -rf /tmp/get-pip.py /var/cache/apk/* /root/.cache 

WORKDIR $WORKSPACE

ENTRYPOINT ansible-playbook $WORKSPACE/main.yml