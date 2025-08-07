FROM amazonlinux:latest
WORKDIR /app

# Install Node.js and npm
RUN yum update && yum install -y nodejs npm

# Copy package.json and package-lock.json first to optimize caching
COPY package*.json ./
RUN npm install

# Copy the rest of the application files
COPY . .

CMD ["npm", "start"]
