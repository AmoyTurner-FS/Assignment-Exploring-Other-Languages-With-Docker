FROM golang:1.22-alpine AS build
WORKDIR /usr/src/myapp
COPY . .
RUN go build -o hello .

FROM alpine:3.19
WORKDIR /usr/src/myapp
COPY --from=build /usr/src/myapp/hello .
CMD ["./hello"]
