# Table of Contents

* [About Trash Coin](#about-Trash-Coin)
* [Features](#features)
* [Guided Tour](#guided-tour)
* [Developer Guide](#developer-guide)
* [Application Design](#application-design)


# About Trash Coin 

Trash Coin is an attempt at designing and implementing 3 popular technology topics into one application. The Trash Coin Project looks at Client/Server interactions, Block Chain frameworks, and data hashing algorithms. 

This application allows users to create a centralized server as well as unique clients.  Server owner will be able to see hash collisions real time, as well as distribution of crypto currency to users. 

# Features

* Create centralized block chain server.
* Create unique clients.
* Adjust collision difficulty.
* Adjust reward amount.
* Client to client crypto currency trading.
* Transaction logging  
* Session Tracking

# Developer Guide

<font color="red"> Warning!!! Project was designed to run on localhost on a unix environment.
Server must be running before Client</font>

Clone or Download the [TrashCoin](https://github.com/TrashBoizLLC/TrashCoin) application. 

## Creating Server

Go to Server directory 

```
$ cd */TrashCoin/Server
```

Compile TrashServer.java using Xlint

```
$ javac TrashServer.java -Xlint 
```

Run TrashCoin Server
```
$ java TrashServer
```
Server will begin, and default to a set port. Port can be changed by going into TrashServer.java and manually changing the port.

## Creating Client

Go to Client directory 

```
$ cd */TrashCoin/Client
```

Compile TrashClient.java using Xlint

```
$ javac TrashClient.java -Xlint 
```
Run TrashCoin Client
```
java TrashClient
```

# Application Design

## Directory structure

The top-level directory structure contains:
```
Client/     # Contains client application sources
Server/     # Contains server application sources
```
This structure separates the necessary application sources for both the server and the client applications. 

The Client/ directory has the following top-level structure:
```
ClientKeys/ # Contains text file copies of client keys
CreateKeys.java # Code to create RSA key pairs
MineBlock.java # Code to guess collisions based on a set difficulty
StringUtil.java # Applies SHA256 to a string and returns the result
TrashClient.java # Main function of application
```

The Server/ directory has the following top-level structure:
```
ClientPubKey/ # Contains copy of clients public keys
Block.java # Class of object block
LoggingFunc.java # Contains code that logs a clients connections
LoginLogoutLog.txt # contains times and dates of client connections
StringUtil.java # Applies SHA256 to a string and returns the result
TrashServer.txt # Contains the main function for the server application
```
