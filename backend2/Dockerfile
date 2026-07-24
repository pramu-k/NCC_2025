# Use lightweight Node.js official image
FROM node:18-alpine

# Set working directory inside container
WORKDIR /app

# Copy package files first to leverage Docker layer caching
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy application source code
COPY . .

# Expose port 5000 (matching server.js port)
EXPOSE 5000

# Command to start the application
CMD ["npm", "start"]
