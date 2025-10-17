# Use official Node.js LTS image
     FROM node:20

     # Set working directory
     WORKDIR /app

     # Copy package.json and package-lock.json
     COPY package*.json ./

     # Install dependencies
     RUN npm install

     # Copy the rest of the frontend code
     COPY . .

     # Build the Vite app for production
     RUN npm run build

     # Install a lightweight server to serve the built app
     RUN npm install -g serve

     # Expose the port for the frontend (match the serve port)
     EXPOSE 3000

     # Command to serve the built app
     CMD ["serve", "-s", "dist", "-l", "3000"]