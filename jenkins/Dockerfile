FROM node:16-alpine

# Install any additional tools you need
RUN apk add --no-cache \
    git \
    openssh-client \
    python3 \
    make \
    g++

# Create and set working directory
WORKDIR /app

# Set npm cache permissions
RUN npm config set cache /tmp --global
