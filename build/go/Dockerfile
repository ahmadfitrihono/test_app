FROM golang:alpine

# Create app directory
WORKDIR /app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY src/go/hello_world.go ./

RUN go mod init hello_world 

RUN go mod tidy

# COPY go.mod ./

# COPY go.sum ./

RUN go build -o /hello_world

ENTRYPOINT [ "./hello_world" ] 