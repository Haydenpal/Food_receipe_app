# Dockerfile for the client
FROM node:16-alpine

WORKDIR /app

# Copy package.json and lock file
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all files
COPY . .

# Set environment variable for React to run on port 3000
ENV PORT=3000

# Expose the client port
EXPOSE 3000

# Run the React development server
CMD ["npm", "start"]
