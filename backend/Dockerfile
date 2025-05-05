# Use Golang as the base image
FROM golang:1.19

# Set working directory
WORKDIR /app

# Copy dependencies and source code
COPY go.mod go.sum ./
RUN go mod download

# Copy the application code
COPY . .

# Build the Go application
RUN go build -o server .

# Expose port and start the application
EXPOSE 8080
CMD ["./server"]