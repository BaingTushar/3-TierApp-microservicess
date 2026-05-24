FROM node:14-alpine

# Create app directory
WORKDIR /usr/src/app

# Copy dependency files first
COPY package*.json ./

# Install only production dependencies
RUN npm install --only=production

# Copy source code
COPY . .

# Expose application port
EXPOSE 3500

# Start application
CMD ["node", "index.js"]
