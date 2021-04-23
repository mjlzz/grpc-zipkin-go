# zipkin-go grpc demo

## docs

[Go微服务全链路跟踪详解](https://zhuanlan.zhihu.com/p/79419529)


[zipkin-go github](https://github.com/openzipkin/zipkin-go)


[zipkin-go api doc](https://pkg.go.dev/github.com/openzipkin/zipkin-go)


[zipkin-go http example](https://github.com/openzipkin/zipkin-go/blob/master/examples/httpserver_test.go)



## demo

1. start zipkin
```bash
docker run -d -p 9411:9411 openzipkin/zipkin
```

2. start grpc server
```bash
go run server/server.go
```

3. send grpc request with trace info
```bash
go run client/client.go
```

4. send grpc request without trace info
```bash
go run client/client_no_zipkin.go
```

5. search on web
localhost:9411