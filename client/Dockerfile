# Use an optimized and stable base image (replace with appropriate Node version as needed)
FROM node:18-alpine3.17

# Set the working directory inside the container
WORKDIR /app

# Copy only dependency-related files to leverage Docker caching
COPY package*.json ./

# Install dependencies
RUN npm install --legacy-peer-deps

# Copy application code
COPY . .

# Build the application
RUN npm run build

# Expose the application port
EXPOSE 3000

# Command to run your application
CMD ["npm", "start"]
