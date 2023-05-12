# go-grpc

This repository aims to study the behavior of gRPC and understand its functioning by implementing a gRPC server using Go. The focus of the study includes creating both unidirectional and bidirectional streaming communication channels. For observing the client-side behavior, the evans tool was utilized.
Table of Contents

   * Introduction to gRPC
   * Server Implementation
   * Database Configuration
   * Running the Server
   * Client-side Behavior with Evans
   * Conclusion


## Introduction to gRPC

gRPC is an open-source remote procedure call (RPC) framework developed by Google. It enables efficient communication between different services by defining a service contract using Protocol Buffers (protobuf). gRPC supports multiple programming languages and provides features like bidirectional streaming, flow control, authentication, and more.
Server Implementation

In this repository, we explore how to create a gRPC server using Go. The server implementation involves defining the service contract using protobuf, implementing the generated interface, and handling the service requests.

To create a gRPC server in Go, follow these steps:

1. Define the service contract using Protocol Buffers. This includes specifying the message types and service methods.
2. Generate Go code from the .proto file using the protoc compiler and the Go plugin for gRPC.
3. Implement the generated interface in Go, fulfilling the requirements of each service method.
4. Set up the server to listen on a specific port and handle incoming gRPC requests.
5. Build and run the server.

The server implementation in this repository serves as a starting point for understanding the basics of creating a gRPC server using Go.


## Database Configuration

The server in this repository utilizes SQLite3 as the database. To set up the necessary table, execute the following SQL statement:

```sql

CREATE TABLE categories (
    id STRING,
    name STRING,
    description STRING
);
```

Create a file named db.sqlite in the root directory of the project or in the directory where main.go file is located.


## Running the Server

To run the gRPC server, execute the following command in the terminal:

```bash

go run cmd/grpcServer/main.go
```
This will start the server and it will be ready to handle incoming gRPC requests.


## Client-side Behavior with Evans

To observe the behavior of the gRPC server from the client's perspective, we utilize the evans tool. Evans is a command-line-based gRPC client that allows you to interact with gRPC services interactively.

With evans, you can perform various operations like invoking service methods, inspecting the service schema, and exploring the available gRPC functionalities. It provides an interactive shell where you can input requests and receive responses from the gRPC server.

By utilizing evans during the development process, you can gain insights into how the client interacts with the gRPC server and validate the behavior of your implemented services.


## Conclusion

This repository serves as a study project for understanding the behavior and functionality of gRPC in Go. It covers the creation of a gRPC server, including unidirectional and bidirectional streaming communication channels. The evans tool is used to observe the client-side behavior and interaction with the server.

By exploring this repository, developers can gain valuable knowledge about working with gRPC, understanding its concepts, and implementing gRPC services using Go.