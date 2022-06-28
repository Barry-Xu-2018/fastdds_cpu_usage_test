# fastdds_cpu_usage_test
This program is used to estimate cpu consumption.   

The original codes are from fastdds/src/fastrtps/examples/C++/DDS/HelloWorldExample.  
The change is 
1. Add topic key and 512 bytes array.
2. User can specify the topic key instead of send interval.

## How to build  

```bash
$ mkdir build && cd build
$ cmake ..
$ make
```

## Run publisher

```bash
$ cd build
$ ./DDSHelloWorldExample publisher 100 1
```
100 means the number of sent message. The interval of sending is 100ms.  
1 means topic key value.  

You can run multi publishers with different topic key.

## Run subscriber
```bash
$ cd build
$ ./DDSHelloWorldExample subscriber
```
