# Golang Beginner Using Docker

This template is designed to help you get started with Go and Docker. Follow the steps below to set up your development environment and run your first Go application inside a Docker container.

## Prerequisites

Before you begin, make sure you have the following installed on your system:

- [Go](https://golang.org/doc/install) (version 1.24 or later)
- [Docker](https://docs.docker.com/get-docker/)

## Installation Guide

### Step 1: Clone the Repository

First, clone this repository to your local machine using the following command:

```sh
git clone https://github.com/jaygaha/go-docker-beginner-template.git
cd go-docker-beginner-template
```

### Step 2: Write Your First Go Program

Create a new Go file named `main.go` in the project directory with the following content:

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```

### Step 3: Dockerfile template

Create a `Dockerfile` in the project directory with the following content:

```Dockerfile
# Use the official Golang image
FROM golang:1.24

# Set the working directory inside the container
WORKDIR /var/www/html

# Copy the Go source code to the container
COPY . .

# Build the Go application
RUN go build -o main .

# Command to run the executable
CMD ["./main"]
```

### Step 4: Build the Docker

Build using docker compose command:

```sh
docker compose build
```

OR

Build the Docker image using the following command:

```sh
docker build -t golang-beginner .
```

### Step 5: Run the Docker Container

Run using docker compose command:

```sh
docker compose up -d
```

OR

Run the Docker container using the following command:

```sh
docker run --rm golang-beginner
```

You should see the output `Hello, World!` in your browser.

## Conclusion

Congratulations! You have successfully set up a Go development environment and run your first Go application inside a Docker container. Feel free to explore and modify the code to learn more about Go and Docker.

Happy coding!

## License

This project is licensed under the [MIT License](LICENSE)
