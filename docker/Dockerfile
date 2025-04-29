FROM ubuntu:24.04

# Install basic dependencies
RUN apt-get update && apt-get install -y \
    python3 \
    bash \
    python3-pip \
    python3-venv \
    build-essential \
    software-properties-common \
    libncurses-dev \
    && rm -rf /var/lib/apt/lists/*

# Change shell to bash
SHELL ["/bin/bash", "-c"]

# Add the Potassco PPA and install clingo + development libraries
RUN add-apt-repository ppa:potassco/stable \
    && apt-get update

RUN apt install -y clingo libclingo-dev libncurses-dev

RUN python3 -m venv /venv
ENV PATH="/venv/bin:$PATH"
RUN pip install --upgrade pip setuptools
RUN pip install pasp-plp torch

# Default command
CMD ["/bin/bash"]
