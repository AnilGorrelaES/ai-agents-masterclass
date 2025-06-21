FROM n8nio/n8n

# Switch to root to install packages
USER root

# Install Python 3 and common build tools (gcc, musl-dev, etc.)
RUN apk add --no-cache \
    python3 \
    py3-pip \
    py3-setuptools \
    py3-wheel \
    python3-dev \
    build-base \
    libffi-dev \
    openssl-dev \
    cmake \
    ninja \
    git \
    openblas-dev \
    linux-headers

# Create and activate virtualenv
RUN python3 -m venv /opt/venv && \
    /opt/venv/bin/pip install --upgrade pip setuptools wheel

# Make venv accessible to PATH
ENV PATH="/opt/venv/bin:$PATH"

# Switch back to node user
USER node
