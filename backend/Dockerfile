# Use a slim Node image for a smaller footprint
FROM node:18-slim

# Create app directory
WORKDIR /app

# Copy dependency definitions
COPY package*.json ./

# Install production dependencies
RUN npm install --only=production

# Copy the rest of your backend code
COPY . .

# Expose the port your backend runs on (e.g., 5000)
EXPOSE 5000

# Start the application
CMD ["npm", "start"]