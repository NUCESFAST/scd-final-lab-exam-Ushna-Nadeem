# Classrooms/Dockerfile
FROM node:14-alpine

# Set the working directory
WORKDIR /i211225_backend/classrooms

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on
EXPOSE 3226

# Start the application
CMD ["node", "index.js"]
