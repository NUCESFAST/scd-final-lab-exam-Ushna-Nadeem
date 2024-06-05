# client/Dockerfile
FROM node:14-alpine

# Set the working directory
WORKDIR /i211225_frontend

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the frontend assets
RUN npm run build

# Expose the port the app runs on
EXPOSE 1225

# Start the application
CMD ["npm", "start"]
