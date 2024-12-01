FROM node:18-alpine

# Install dependencies required for building bcrypt and node-gyp
RUN apk add --no-cache \
    python3 \
    make \
    g++ \
    bash \
    && npm install -g nodemon

# Create and switch to a non-root user

# Set the working directory
WORKDIR /app

# Copy the package.json and package-lock.json files
COPY package.json package-lock.json ./

# Change ownership of the app directory and all its files to appuse

# Install project dependencies
RUN npm install 

# Rebuild bcrypt specifically for the container's architectur
# Copy the rest of the application files
COPY . .

# Expose the port the server is running on
EXPOSE 3001

# Start the server using nodemon
CMD ["npm", "start"]
