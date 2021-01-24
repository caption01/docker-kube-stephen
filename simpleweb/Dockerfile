# Specify a base image
FROM node:alpine

WORKDIR /usr/app

# Copy package.json file
COPY ./package.json ./

# Install some dependencies
RUN npm install

# Copy source file
COPY ./ ./

# Default CMD
CMD ["npm", "run", "start"]

