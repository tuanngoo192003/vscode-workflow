# FROM golang:1.24-bookworm
# golang:1.24-trixie
FROM golang:1.24

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
    git \
    curl \
    wget \
    unzip \
    make \
    vim \
    net-tools \
    iputils-ping \
    jq \
    bash \
    tar \
 && rm -rf /var/lib/apt/lists/*

# Install kubectl (latest stable)
RUN KUBECTL_VERSION=$(curl -sSL https://dl.k8s.io/release/stable.txt) && \
    curl -sSL "https://dl.k8s.io/release/${KUBECTL_VERSION}/bin/linux/amd64/kubectl" \
      -o /usr/local/bin/kubectl && \
    chmod +x /usr/local/bin/kubectl

# Install kind (latest release)
RUN KIND_VERSION=$(curl -s https://api.github.com/repos/kubernetes-sigs/kind/releases/latest | jq -r .tag_name) && \
    curl -Lo /usr/local/bin/kind "https://kind.sigs.k8s.io/dl/${KIND_VERSION}/kind-linux-amd64" && \
    chmod +x /usr/local/bin/kind

# Install kustomize (fixed version)
RUN KUSTOMIZE_VERSION=v5.5.0 && \
    curl -sSL "https://github.com/kubernetes-sigs/kustomize/releases/download/kustomize/${KUSTOMIZE_VERSION}/kustomize_${KUSTOMIZE_VERSION}_linux_amd64.tar.gz" \
      -o /tmp/kustomize.tar.gz && \
    tar -xzf /tmp/kustomize.tar.gz -C /usr/local/bin && \
    rm /tmp/kustomize.tar.gz

WORKDIR /work
