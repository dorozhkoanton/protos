# protos
protos

## Install protoc
```
brew install protobuf

go install google.golang.org/protobuf/cmd/protoc-gen-go@1.36.6
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@1.5.1

export PATH="$PATH:$(go env GOPATH)/bin"
```

## Generate code
`protoc -I proto proto/sso/sso.proto --go_out=./gen/go --go_opt=paths=source_relative --go-grpc_out=./gen/go --go-grpc_opt=paths=source_relative`
