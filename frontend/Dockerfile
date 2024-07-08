# Use the latest Node.js image
FROM node:latest

# Set the working dir
WORKDIR /app

# Copy the files
COPY . .

# Install dependencies
RUN npm install

# Expose the server port 
EXPOSE 5173

# Run the dev server
CMD ["npm", "run", "dev", "--", "--host"]