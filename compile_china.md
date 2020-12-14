## compile process

### compile gRpc

compile grpc into `$HOME/.local`

doc: `https://grpc.io/docs/languages/cpp/quickstart/`

### edit gradle.properties

```shell
touch gradle.properties
echo 'skipAndroid=true' >> gradle.properties
```

### compile grpc-java

```shell
 export CXXFLAGS="-I/home/chuande/.local/include" LDFLAGS="-L/home/chuande/.local/lib"

 ./gradlew build --parallel -x test
 
 
 ./gradlew publishToMavenLocal
```

### compile grpc-java example

```shell
./gradlew installDist
```
