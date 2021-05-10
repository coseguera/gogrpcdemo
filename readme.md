# Golang gRPC demo
Follows tutorial from https://grpc.io/docs/languages/go/basics/

## Steps performed
```
go mod init github.com/coseguera/gogrpcdemo
mkdir routeguide
go get google.golang.org/grpc
go get google.golang.org/protobuf/reflect/protoreflect@v1.25.0
```

## To generate the protobuf
```
protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative routeguide/route_guide.proto 
```

## To run
```
go run server/server.go 
go run client/main.go 
```