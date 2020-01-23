FROM python:3.8-buster

RUN groupadd --gid 1000 ansible && useradd --uid 1000 -g ansible ansible

COPY tini /tini
ENTRYPOINT ["/tini", "--" ]

# see: https://pypi.org/project/ansible/
ARG ANSIBLE_VERSION=2.9.4

RUN pip3 install ansible==${ANSIBLE_VERSION}

USER 1000
