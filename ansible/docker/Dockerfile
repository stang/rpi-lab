FROM python:3.8-buster

RUN groupadd --gid 1000 ansible && useradd --uid 1000 -g ansible ansible

COPY tini /tini
ENTRYPOINT ["/tini", "--" ]

# Note: we're not using 'ADD' as there are some caching issues
# see: https://github.com/moby/moby/issues/15717

# see: https://hub.docker.com/r/bitnami/kubectl/tags
COPY --from=bitnami/kubectl:1.17.2 /opt/bitnami/kubectl/bin/kubectl /usr/local/bin/kubectl

# see: https://pypi.org/project/ansible/
ARG ANSIBLE_VERSION=2.9.4

RUN pip3 install ansible==${ANSIBLE_VERSION}

USER 1000
