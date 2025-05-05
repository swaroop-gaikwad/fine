# Use Node.js as the base image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy dependencies and install them
COPY package.json package-lock.json ./
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the frontend application
RUN npm run build

# Expose port and start the application
EXPOSE 3000
CMD ["npm", "start"]