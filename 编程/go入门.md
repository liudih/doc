常用命令
=====
macbook:
```go
go version
go env

#还原环境变量
go env -u GO111MODULE
#设置环境变量
go env -w GO111MODULE=on
#设置代理
go env -w GOPROXY=https://goproxy.cn,direct
or
go env -w GOPROXY=https://goproxy.io

mkdir test
goland test

go run main.go
go mod init liudi.com/test
go get -u github.com/gin-gonic/gin
# 安装项目依赖
go get

```