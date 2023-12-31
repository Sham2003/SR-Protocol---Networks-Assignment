# Selective Repeat

Implementing SR protocol of the udp to transfer a video file.

## Description

The protocol is made reliable using the following techniques:
* Sequence numbers
* Retransmission (selective repeat)
* Window size of 5-10 UDP segments (stop n wait)
* Re ordering on receiver side

## Getting Started

### Dependencies

* C++
* Linux

### Installing

* Clone the repo
```

```
* change dir to reliableUDP then specify the port number and the video file you want to use in **client.c and server.c** . Also change the server ip in case of LAN.
```
#define VIDEO_FILE "testFiles/sampleVideo.mp4"
#define PORT 2003
#define SERVER_ADDR "192.168.112.94"
```  

### Executing program

* Start the server first
```
gcc server.c -o server
./server
```
* Then start the client
```
gcc client.c -o client
./client
```
