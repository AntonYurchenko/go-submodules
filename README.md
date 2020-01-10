# Description
The example shows how you can use one repository for some submodules written on GO. 
Each submodule has unique tag, for example:
```bash
git clone https://github.com/AntonYurchenko/go-submodules
cd go-submodules
git tag -l
# app/v0.0.1
# lib/v0.0.1
```

## Start example
```bash
git clone https://github.com/AntonYurchenko/go-submodules
cd go-submodules
GOPRIVATE='github.com' go run app/main.go
# 22:02:04
```
If you don't set environment `GOPRIVATE` you will catch error:
```text
verifying github.com/AntonYurchenko/go-submodules/lib@v0.0.1/go.mod: github.com/AntonYurchenko/go-submodules/lib@v0.0.1/go.mod: reading https://sum.golang.org/lookup/github.com/!anton!yurchenko/go-submodules/lib@v0.0.1: 410 Gone
```

## GO version
```bash
go version
# go version go1.13.1 darwin/amd64
```