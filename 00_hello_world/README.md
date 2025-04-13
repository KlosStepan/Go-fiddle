# Hello World

## Getting ready
```
go mod init hello_world
touch main.go
vim main.go
```
You can manually run program as
```
go run main.go
```
## VS Code - F5 compile+run support
Install dlv
```
go install -v github.com/go-delve/delve/cmd/dlv@latest
```
Check $GOPATH
```
echo $GOPATH
```
Export $GOPATH
```
export PATH=$PATH:$GOPATH/bin
```
Echo $PATH should include you Go installation chosen in GVM.
```
echo $PATH
```
