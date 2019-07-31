# Use this empty Dockerfile to build your assignment.

# This dir contains a Node.js app, you need to get it running in a container.
# No modifications to the app should be necessary, only edit this Dockerfile.

# Overview of this assignment.
# Use the instructions from developer below to create a working Dockerfile.
# Feel free to add command inline below or use a new file, up to you. (but must be named Dockerfile)
# Once Dockerfile builds correctly, start container locally to make sure it works on http://localhost.
# Then ensure image is named properly for your Docker Hub account with a new repo name.
# Push to Docker Hub, then go to https://hub.docker.com and verify.
# Then remove local image from cache.
# Then start a new container from your Hub image, and watch how it auto downloads and runs.
# Test again that it works at http://localhost.


# Instructions from the app developer.
# - You should use the 'node' official image, with the alpine 6.x branch.
FROM node:6-alpine
# - This app listens on port 3000, but the container should launch on port 80 so it will respond to http://localhost:80 on your computer.
EXPOSE 3000
# - Then it should use alpine package manager to install tini: 'apk add --update tini'.
RUN apk add --update tini
# - Then it should create directory /usr/src/app for app files with 'mkdir -p /usr/src/app'.
RUN mkdir -p /usr/src/app
# - Node uses a "package manager", so it needs to copy in package.json file.
WORKDIR /usr/src/app
COPY package.json package.json
# - Then it needs to run 'npm install' to install dependencies from that file.
RUN npm install && npm cache clean
# - To keep it clean and small, run 'npm cache clean --force' after above.
# - Then it needs to copy in all files from current directory.
COPY . .
# - Then it needs to start container with command '/sbin/tini -- node ./bin/www'.
CMD [ "tini", "--", "node", "./bin/www" ]
# - In the end you should be using FROM, RUN, WORKDIR, COPY, EXPOSE, and CMD commands.

# Bonus Extra Credit.
# This will not have you setting up a complete image useful for local development, test, and prod.
# It's just meant to get you started with basic Dockerfile concepts and not focus too much on proper Node.js use in a container. **If you happen to be a Node.js Developer**.