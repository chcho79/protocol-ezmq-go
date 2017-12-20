# ezMQ GO Client SDK

protocol-ezmq-go library provides a standard messaging interface over various data streaming 
and serialization / deserialization middlewares along with some added functionalities.</br>
Following is the architecture of ezMQ client library: </br> </br>
![ezMQ Architecture](doc/images/ezMQ_architecture_0.1.png?raw=true "ezMQ Arch")

## Features:
* Currently supports streaming using 0mq and serialization / deserialization using protobuf.
* Publisher -> Multiple Subscribers broadcasting.
* Topic based subscription and data routing at source (read publisher).
* High speed serialization and deserialization.

## Future Work:
* High speed parallel ordered serialization / deserialization based on streaming load.
* Threadpool for multi-subscriber handling.
* Router pattern.
* Clustering Support.
</br></br>

## How to build ezMQ SDK and samples
### pre-requisites
1. go 1.9 should be installed on linux machine. </br>
   **Refer:** https://golang.org/doc/install

### Build Instructions
1. Goto: ~/protocol-ezmq-go/
2. ./build.sh </br>
   **Note:** For getting help about script: **$ ./build.sh --help**

## How to run ezMQ samples

### pre-requisites
Built ezMQ
### Run the subscriber sample application

1. Goto: ~/${GOPATH}/src/go/samples/
2. ./subscriber
3.  On successful running it will show following logs:

```
Initialize API [result]: 0
```
**Follow the instructions on the screen.**

###  Run the publisher sample application

1. Goto: ~/${GOPATH}/src/go/samples/
2. ./subscriber
3.  On successful running it will show following logs:

```
Initialize API [result]: 0
```
**Follow the instructions on the screen.**

## ezMQ Usage guide [For micro-services]
1. The micro-service which wants to use EZMQ GO SDK has to import ezmq package:
    - import go/ezmq
2. Refer EZMQ sample applications to use EZMQ SDK APIs. **[~/EZMQ/go/samples]**

## Generating godoc for ezMQ  SDK 
1. After installing the EZMQ go SDK, godoc can be generated using following command: </br>
   $ godoc -html go/ezmq  > ezmq.html
2. Open the ezmq.html in web browser. </br>
    **Note:** Refer [guide]( https://godoc.org/golang.org/x/tools/cmd/godoc) for trying more options.

## Running static analyzer for ezMQ SDK
1. Goto: ~/${GOPATH}/src/go/
2. Run the below command:
   $ go tool vet -all .
