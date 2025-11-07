FROM node:20
# Create application directory
RUN mkdir /opt/server
# Set working directory
WORKDIR /opt/server

# Environment variable for DB connection
ENV DB_HOST="mysql"

# Copy dependency files & install dependencies
COPY package.json .
COPY *.js .
RUN npm install 

# Create non-root user and switch
RUN useradd expense && chown -R expense:expense /opt/server
USER expense

# Expose app port
EXPOSE 8080

# Start the Node.js app
CMD ["node", "index.js"]
