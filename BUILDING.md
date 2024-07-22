Building Tongsuo-Java-SDK
==================

Before you begin, you'll first need to properly configure the [Prerequisites](#Prerequisites) as
described below.

Then to build, run:

```bash
$ ./gradlew build -PtongsuoHome=/opt/tongsuo
```

To publish the artifacts to your Maven local repository for use in your own project, run:

```bash
$ ./gradlew publishToMavenLocal -PtongsuoHome=/opt/tongsuo
```

Prerequisites
-------------
Tongsuo-Java-SDK requires that you have __Java__, __Tongsuo__ configured as described
below.

#### Java
The build requires that you have the `JAVA_HOME` environment variable pointing to a valid JDK.


#### Tongsuo
Download Tongsuo and then build as follows:

```bash
git clone https://github.com/Tongsuo-Project/Tongsuo.git
cd Tongsuo
git checkout 8.4-stable

./config no-shared enable-ntls enable-weak-ssl-ciphers --release --prefix=/opt/tongsuo --libdir=/opt/tongsuo/lib
make -j
make install
```

Running tests
-------------------------

```bash
./gradlew test -PtongsuoHome=/opt/tongsuo
```

Coverage
--------
To see coverage numbers, run the tests and then execute the jacocoTestReport rule

```bash
./gradlew check jacocoTestReport -PtongsuoHome=/opt/tongsuo
```

The report will be placed in `openjdk/build/reports/jacoco/test/html/index.html`
