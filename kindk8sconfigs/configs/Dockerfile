FROM ubuntu:latest
WORKDIR /root
RUN mkdir .kube && \
apt-get update && \
apt install -y git && \
apt-get install -y apt-transport-https ca-certificates curl && \
curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg && \
echo "deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | tee /etc/apt/sources.list.d/kubernetes.list && \
apt-get update && \
apt-get install -y kubectl=1.19.11-00
ENTRYPOINT ["tail", "-f", "/dev/null"]
COPY config /root/.kube/config
