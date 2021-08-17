FROM node:10.16.0-alpine as builder

# Create app directory
WORKDIR /app

# Install app dependencies
COPY package*.json  /app/

# Install all app dependencies
RUN npm install

# Copy project files into the docker image
COPY . /app

# Build as Prod Build (can be customized as per project requirment)
RUN npm run build -- --prod
