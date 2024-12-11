# Use the official Node.js image as the base image
FROM node:alpine

# Set the working directory
WORKDIR /src/app

# Copy the package.json and package-lock.json files
COPY package*.json ./

# Install the dependencies
RUN npm install

# Install Angular CLI globally
RUN npm install -g @angular/cli

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on (8080)
EXPOSE 8080

# Start the Angular application in development mode on port 8080
CMD ["ng", "serve", "--host", "0.0.0.0", "--port", "8080"]
