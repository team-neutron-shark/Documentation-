# Team Neutron Shark Documentation

## New Contributor Info

This project is a Unity-based client for the Keyforge card game. Currently, the project is divided into two efforts: a Go server and a Unity-client programmed in C#.

Contributors that would like to help with server should look at the repo housed [here](https://github.com/team-neutron-shark/keyforge-network).

Contributors that would like to help with the Unity Client should look [here](https://github.com/team-neutron-shark/keyforge-client). The client will need an instance of the server running, but this can be accomplished through Docker.

## Docker Info

Contributors can use a [Docker Community license and install Docker Desktop](https://www.docker.com/get-started).

**Warning:** The Windows version of Docker Desktop requires Windows Pro or Enterprise to function. 

Once Docker Desktop is running, the following two commands will get a local server instance running:

```
docker pull sigmaseven/keyforge-network-server
docker run -it sigmaseven/keyforge-network-server
```

The server can be terminated with `Ctrl+C`

## Go Language Installation

To run the server locally without Docker, Go will need to be installed.

The instructions to install Go can be found [here](https://golang.org/doc/install).

## Running the Go Server Locally

With Go installed, this command can be run from the `users/[yourname]` folder:

```
go get github.com/team-neutron-shark/keyforge-network
```

This will install the repo locally. The filepath for the keyforge-network repo should look like this:

```
users/[yourname]/go/src/github.com/team-neutron-shark/keyforge-network
```

If the file path does not resemble this, the [GOPATH variable may be misconfigured](https://github.com/golang/go/wiki/SettingGOPATH). 

From the repo, this command will build the server:

```
go build server/kfserver.go
```

kfserver.exe should now be in the base repo folder. Running this file will now start a local instance of the server.

## Building the Text Client

Currently, the only purpose of the text client is to test the server while the Unity client is under construction.

Building the text client is similar to building the server, and if the instructions up to this point have been followed, this command can be run from the keyforge-network repo:

```
go build client/kfclient.go
```

kfclient.exe should now be located alongside the kfserver.exe. 