# Start from official Node.js base image
FROM node:16-alpine

# (Optional) Install Docker CLI if needed inside this image
RUN apk add --no-cache docker

# (Optional) Install other tools
# RUN apk add --no-cache git curl bash

# Set work directory (not required, but good practice)
WORKDIR /app

# (Optional) Default command
CMD [ "node" ]
