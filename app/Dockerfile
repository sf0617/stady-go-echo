FROM golang:1.16-alpine

RUN apk update
RUN apk --no-cache add curl

ENV GO111MODULE=on

WORKDIR /usr/src/app/stady-go-echo
# 本番運用時はソースをコピーして配置
# COPY ./ ./
# RUN go mod download

# 以下、Golang 開発環境用
# ホットリロード(freshのインストール))
RUN go install github.com/pilu/fresh@latest

RUN go install github.com/go-delve/delve/cmd/dlv@latest
RUN go install github.com/rogpeppe/godef@latest
RUN go install golang.org/x/tools/cmd/goimports@latest
RUN go install golang.org/x/tools/cmd/gorename@latest
RUN go install sourcegraph.com/sqs/goreturns@latest
RUN go install github.com/ramya-rao-a/go-outline@latest
RUN go install golang.org/x/tools/gopls@latest
