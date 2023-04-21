FROM golang:1.20-bullseye as builder

COPY ./main.go main.go

RUN go build -o main main.go

FROM scratch

COPY --from=builder /go/main .

CMD ["./main"]