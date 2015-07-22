# Standalone etcd server

## docker run / docker start

This example sets up a standalone etcd server. Docker helper scripts are

```bash
./run-etcd
./start-etcd
./stop-etcd
```

where `run-etcd` creates the container using `docker run` and `start-etcd` starts an existing container using `docker start`. The container is named `etcd` and the single etcd member that is started is named `etcd0`.

## API access

In order to test the etcd service, the following scripts can be used:

```bash
./version
./leader
./members
```

where `version` prints the etcd version in use (currently `v2.1.1`), `leader` prints the current cluster leader (which is this instance) and `members` prints the current cluster members (which is also just this instance).

If `jsonpp` is installed (e.g. using the `jsonpp-bin` AUR package on Arch Linux), then the API result is formatted on output.
