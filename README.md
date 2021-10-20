# envoy-proxy-wasm-filter-golang
A WASM Filter for Envoy Proxy written in Golang

# Build

```tinygo build -o optimized.wasm -scheduler=none -target=wasi ./main.go```

# Run Envoy Proxy in Docker with WASM Filter

```docker run -it --rm -v "$PWD"/envoy.yaml:/etc/envoy/envoy.yaml -v "$PWD"/optimized.wasm:/etc/envoy/optimized.wasm -p 9901:9901 -p 10000:10000 envoyproxy/envoy:v1.17.0```
