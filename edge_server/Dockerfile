# Use a lightweight base image
FROM alpine:latest 
LABEL org.opencontainers.image.authors="vishal@orsted.com"
LABEL org.opencontainers.image.source=https://github.com/vishyVishal/container-fundamentals
LABEL org.opencontainers.image.description="Containter Fundamentals - Static Website Image"
LABEL org.opencontainers.image.licenses=APACHE2

# Install nginx
RUN apk --no-cache add nginx

# Copy config and web content
COPY config/nginx.conf /etc/nginx/
COPY web_content/ /var/www

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

