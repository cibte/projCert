# Start with a base image that includes PHP and Apache
FROM php:7.4-apache

# Set the working directory
WORKDIR /var/www/html

# Copy the application code to the container
COPY . /var/www/html

# Install any dependencies required by the application
RUN apt-get update && \
    apt-get install -y \
        git \
        zip \
        unzip && \
    docker-php-ext-install pdo_mysql

# Expose the port used by Apache
EXPOSE 80

# Start Apache
CMD ["apache2-foreground"]
