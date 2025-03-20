# Use the official NGINX image
FROM nginx:latest

# Remove the default NGINX config
RUN rm /etc/nginx/nginx.conf 

# Copy the custom NGINX config file
COPY nginx.conf /etc/nginx/nginx.conf

# Create a directory for SSL certificates
RUN mkdir -p /etc/nginx/ssl

# Copy self-signed SSL certificates into the container
COPY certs/selfsigned.crt /etc/nginx/ssl/selfsigned.crt
COPY certs/selfsigned.key /etc/nginx/ssl/selfsigned.key

# Expose HTTP and HTTPS ports
EXPOSE 80 443
