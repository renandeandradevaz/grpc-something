

Generate golang files:

```
export GO111MODULE=on
go get google.golang.org/protobuf/cmd/protoc-gen-go
go get google.golang.org/grpc/cmd/protoc-gen-go-grpc
export PATH="$PATH:$(go env GOPATH)/bin"
protoc --go_out=. --go_opt=paths=source_relative \
    --go-grpc_out=. --go-grpc_opt=paths=source_relative \
    grpcsomethingproto/grpc-something.proto
```



Run server:

```
cd server
go run main.go
```

Run client:

```
cd client
go run main.go
```