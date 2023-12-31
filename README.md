implementation of grpc-web using react, courtesy of adjoeio: https://github.com/adjoeio/grpc-react/tree/main

## Description

This is an example repo to call a grpc service from a react client, inspired by [this this repo](https://github.com/norbjd/grpc-web-nginx-envoy)

1. client is on port `8081` and calls Envoy proxy on port `8000`
2. envoy proxy on port `8000` calls grpc service on port `50051`

## Run

To run the stack:

```
docker-compose build
docker-compose up
```

Then, in a browser, open [`http://localhost:8081`](http://localhost:8081) (the client using gRPC-web to call Envoy).

Enter a name in the input and you should see:

```
Hello {entered_name}!
```

I'm using create-react-app with typescript and grpc-web, grpc & proto generated with bellow command in the root:

```
./proto-gen-grpc-web.sh
```
# grpc-react
implementation of grpc-web using react, initial commit courtesy of adjoeio

to run: 
start docker;
in terminal - 
cd to root directory of folder,
run: docker-compose build,
run: docker-compose up,
after build is finishing and dev server is running navigate to localhost 8081
