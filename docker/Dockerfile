# Stage 1: Build the Go binary
FROM golang:1.24 AS builder

# Set the working directory inside the container
WORKDIR /app

# Copy go.mod and go.sum first (better for caching dependencies)
COPY go.mod go.sum ./

# Download dependencies
RUN go mod download

# Copy the rest of the application
COPY ../ .

# Build the Go app
RUN CGO_ENABLED=0 go build -o hello .

# Stage 2: Create a small runtime image
FROM alpine:3.22.1

# Set the working directory inside the container
WORKDIR /root/

# Copy the prebuilt binary from the builder stage
COPY --from=builder /app/hello .

# Run the binary
CMD ["./hello"]
