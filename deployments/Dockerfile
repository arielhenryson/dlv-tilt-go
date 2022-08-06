FROM golang:1.16-alpine
RUN apk add build-base

RUN go get github.com/go-delve/delve/cmd/dlv

WORKDIR /app

COPY . .

RUN go build -gcflags "-N -l" -o /example-go

#CMD /example-go
CMD dlv debug --headless --log -l 0.0.0.0:2345 --api-version=2 --accept-multiclient