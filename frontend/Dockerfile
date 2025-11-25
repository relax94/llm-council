FROM node:20-slim

WORKDIR /app

# Copy package files first for better caching
COPY package*.json ./
RUN npm install

# Copy frontend code
COPY . .

# Expose the port
EXPOSE 5173

# Run the dev server with host binding for Docker
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]