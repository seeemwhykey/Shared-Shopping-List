FROM node:8

# Create app directory
WORKDIR /usr/src/app

# Install json-server
RUN npm install -g json-server

# Copy the app
COPY . .

# Expose the port used by http server, so other containers can access it
EXPOSE 3000

# starting point when the image is executed
CMD ["json-server", "-H0.0.0.0", "--watch", "db.json"]
