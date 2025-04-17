### GRPC
How to generate

- install lib
```bash
npm i -g protoc-gen-grpc-web protoc-gen-js
```
- Build command
```bash
protoc -I=./proto \
 --js_out=import_style=commonjs,binary:./gen/js \
 --grpc-web_out=import_style=typescript,mode=grpcwebtext:./gen/js \
 ./proto/connect.proto
```
