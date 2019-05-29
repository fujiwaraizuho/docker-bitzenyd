Bitzenyd Docker Image
=====================

# Image

Repo: `fujiwaraizuho/bitzenyd:tag`
Tag:

- `latest` - Debian latest version

! now work to host docker image on Organizaion.

# How to use

1.Create data directory.

```
$ mkdir bitzeny-data
```

2.Create file at `bitzeny-data/bitzeny.conf`.

```
rpcuser=rpc
rpcpassword=rpcpass
rpcallowip=localhost
server=1
```

3. Run docker container with volume option

```
docker run --name bitzenyd -d -v bitzeny-data:/root/.bitzeny -p 9252:9252 fujiwaraizuho/bitzenyd:latest
```
