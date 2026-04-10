FROM node:18-slim

# Add this to fix the 10 Debian vulnerabilities (gpgv, libc6, openssl, etc.)
RUN apt-get update && apt-get upgrade -y && apt-get clean
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