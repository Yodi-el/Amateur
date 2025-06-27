FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Install system packages
RUN apt-get update && \
    apt-get install -y \
        build-essential \
        gcc \
        g++ \
        python3 \
        python3-pip \
        nodejs \
        npm \
        curl \
        git \
        vim && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

# Install Python tools
RUN pip3 install pylint

# Install global Node tools (optional)
RUN npm install -g eslint

# Clone dotfiles repo if it exists (customize this URL)
RUN git clone https://github.com/your-username/dotfiles.git ~/dotfiles || true

# Set working directory
WORKDIR /workspace
