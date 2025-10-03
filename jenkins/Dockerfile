# Use Node.js 16 on Alpine
FROM node:16-alpine

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm ci

# Copy source code
COPY . .

# Create non-root user (security best practice)
RUN addgroup -S appgroup && adduser -S appuser -G appgroup
USER appuser

# Expose necessary ports
EXPOSE 8080 50000

# Start the Node.js app
CMD ["npm", "start"]

