# Reference code: https://community.n8n.io/t/how-to-install-python-libraries-with-docker-image-to-use-them-in-n8n/91015/2
FROM n8nio/n8n

# Switch to root to install packages
USER root

# Install Python and required build tools
RUN apk add --no-cache \
    python3 \
    py3-pip

# Upgrade pip and create venv
RUN python3 -m ensurepip && \
    pip3 install --no-cache --upgrade pip setuptools wheel

# Add venv to path
ENV PATH="/opt/venv/bin:$PATH"

# Switch back to node user
USER node
