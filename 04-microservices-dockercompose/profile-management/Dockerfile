# Use the official Node.js image as the base image
FROM node:14-slim

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY *.json .

# Install the dependencies
RUN npm install

# Copy the rest of the application source code
COPY . .

# Expose the port that the API listens on
EXPOSE 3003

# Run the Node.js application when the container starts
CMD ["node", "auth_api.js"]