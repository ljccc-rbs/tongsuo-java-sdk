# JCE Examples

Every example in this directory is a standalone example that demonstrates how to use the JCE API in Tongsuo OpenJDK.
The example depends on tongsuo-openjdk. You need to build tongsuo-openjdk or download it from maven repository.
Take TLS13Client and TLS13Server as an example.

## TLS13Client

```shell
cd examples/jce

# build
javac -cp /path/to/tongsuo-openjdk-<version>-<os>-<arch>.jar TLS13Client.java

# run
java -cp .:/path/to/tongsuo-openjdk-<version>-<os>-<arch>.jar TLS13Client
```

## TLS13Server

TLS13Server depends on bouncycastle and tongsuo-openjdk. You need to download bcprov-jdk from maven repository.

Note: sm2.crt, sm2.key and chain.crt are required to run the server.

```shell
cd examples/jce

# build
javac -cp /path/to/bcprov-jdk15on-1.69.jar:/path/to/tongsuo-openjdk-<version>-<os>-<arch>.jar  TLS13Server.java

# run
java -cp .:/path/to/bcprov-jdk15on-1.69.jar:/path/to/tongsuo-openjdk-<version>-<os>-<arch>.jar TLS13Server
```
