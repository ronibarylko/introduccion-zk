FROM sagemath/sagemath:10.8

USER root

# Install packages needed by VS Code Server
RUN apt-get update && apt-get install -y \
    curl \
    git \
    sudo \
    && rm -rf /var/lib/apt/lists/*

# Allow the sage user to use sudo (VS Code Server needs this)
RUN echo "sage ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

# The sagemath kernel is already registered in the base image — no extra setup needed

USER sage
