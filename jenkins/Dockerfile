# ✅ Start FROM official Node.js 16 Alpine image
FROM node:16-alpine

# 🧰 (Optional) Install Docker CLI if you need docker-in-docker
RUN apk add --no-cache docker

# ✅ Confirm node + npm are available
RUN node -v && npm -v

# Set a working directory (optional)
WORKDIR /app

CMD ["sh"]
