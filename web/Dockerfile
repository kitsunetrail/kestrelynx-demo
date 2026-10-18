FROM node:22.12.0-slim
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci --omit=dev
COPY server.js .
CMD ["node", "server.js"]
