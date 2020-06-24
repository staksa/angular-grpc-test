# angular-grpc-test

## Installation

Use Docker Compose to build client, server and proxy together.

    docker-compose build

## Usage

Run client, server and proxy together.

    docker-compose up
    
## Access path

Client site with Angular:

    http://localhost:80/

Server site with Go:

    http://localhost:50051/

Access the Envoy Proxy at:

    http://localhost:8080/

## Protocol Buffers

If you need to modify .proto files, you can go to `./proto` and then you will need to compile them again.

    cd proto
    vim/nano calc.proto
    
    # After modify
    cd ..
    sh ./protoc.sh
    
## Client development mode

The Docker Image will build client with production mode. If you need to use development mode.

    cd ./client
    npm start
    
And the client access path is

    http://localhost:4200/

## Testing endpoints

If you want to try your server endpoint without client and proxy.

    cd ./server/test
    go run main.go