# Step 1: Build the Next.js application
FROM node:18 AS builder

# Set working directory
WORKDIR /app

# Install pnpm globally
RUN npm install -g serve

# Copy the rest of the application
COPY . .


# Step 2: Create the production image
FROM node:18 AS production

WORKDIR /app

# Install pnpm globally
RUN npm install -g serve

# Expose the application port
EXPOSE 7000

# Start the Next.js app
CMD ["npm", "start"]
