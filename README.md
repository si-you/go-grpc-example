# go-grpc-example.

A minimal example shows how to use gRpc in Go + Bazel.

```bash
bazel build -c opt ...
```

Run a server
```
bazel-bin/examples/greeter_server/<your arch>/greeter_server
```

Run a client
```
bazel-bin/examples/greeter_client/<your arch>/greeter_client
```

