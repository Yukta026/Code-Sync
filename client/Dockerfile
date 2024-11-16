# Use the Node.js base image
FROM node:latest

# Set the working directory to /app
WORKDIR /app


# COPY ./client/package*.json /app/
# RUN npm install --production  # Only install production dependencies
# COPY ./client /app/

# Copy package.json and package-lock.json from the client folder to /app directory in the container
COPY client/package*.json ./
COPY ./client /app/
# Install dependencies
RUN npm install

# Copy the entire src folder from the client directory into /src in the container
# COPY client/src /src

# Set environment variable for production
# ENV NODE_ENV=production

# Expose the application port
EXPOSE 5173

# Run the application
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
