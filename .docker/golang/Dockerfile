# Production Dockerfile
# Use the official Golang image
FROM golang:1.24

# Maintainer Info
LABEL org.opencontainers.image.authors="Jay Gaha <https://github.com/jaygaha>" \
org.opencontainers.image.title="Golang Docker Image" \
org.opencontainers.image.description="This is a Golang Docker Image" \
org.opencontainers.image.source="https://github.com/jaygaha/go-docker-beginner-template"

# Set the working directory inside the container
WORKDIR /var/www/html

# Copy the Go source code to the container
COPY . .

# Build the Go application
RUN go build -o main .

# Command to run the executable
CMD ["./main"]