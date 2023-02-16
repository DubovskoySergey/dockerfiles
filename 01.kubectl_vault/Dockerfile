FROM alpine
RUN apk add -X https://dl-cdn.alpinelinux.org/alpine/v3.16/main -u alpine-keys && apk update
RUN apk add vault && apk add --no-cache vault libcap && setcap cap_ipc_lock= /usr/sbin/vault
RUN apk add --update curl && \
    rm -rf /var/cache/apk/*
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl
RUN apk del curl --quiet && rm -rf /var/cache/apk/*
RUN chmod +x ./kubectl && mv ./kubectl /usr/local/bin/kubectl && kubectl version --client