# Use Node.js for the server
FROM node:latest

# Set working directory
WORKDIR /app

COPY ./server/package*.json /app/
RUN npm install --production
COPY ./server /app/

# Copy package.json and install dependencies
# COPY ./server /app/
# RUN npm install



# Expose the server port
EXPOSE 3000

# Start the server
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
