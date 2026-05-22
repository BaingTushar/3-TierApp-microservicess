# Small lightweight image
FROM node:14-alpine

# Create app directory
WORKDIR /usr/src/app

# Copy package files first for layer caching
COPY package*.json ./

# Install only production dependencies
RUN npm install --only=production

# Copy application source
COPY . .

# Expose app port
EXPOSE 3000

# Start application
CMD ["npm", "start"]
