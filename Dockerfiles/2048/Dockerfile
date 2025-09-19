FROM ubuntu:22.04

# Install dependencies
RUN apt-get update && apt-get install -y \
    software-properties-common \
    nginx \
    curl \
    unzip \
 && rm -rf /var/lib/apt/lists/*

# Download and extract website files
RUN curl -L https://codeload.github.com/Soumyakant007/2048/zip/refs/heads/main -o /tmp/master.zip \
 && unzip /tmp/master.zip -d /tmp \
 && mv /tmp/2048-main/* /var/www/html/ \
 && rm -rf /tmp/*

# Expose port 80
EXPOSE 80

# Start nginx in foreground
CMD ["nginx", "-g", "daemon off;"]
