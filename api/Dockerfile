FROM node:16-alpine3.14

# Create app directory
WORKDIR /app

# Install app
COPY package*.json ./
RUN npm ci --only=production

# Bundle app source
COPY . .

# Start server
EXPOSE 8002
USER 1001
CMD [ "node", "--max-http-header-size=64000", "index.js" ]
