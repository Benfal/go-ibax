# IBAX Blockchain System Platform
## - The Most Powerful Infrastructure for Applications on Decentralized/Centralized Ecosystems

A  powerful blockchain system platform with a new system framework and a simplified programming language, it is including smart contract, database table and interface.

### Build from Source

#### Install Go

The build process for go-ibax requires Go 1.12 or higher. If you don't have it: [Download Go 1.12+](https://golang.org/dl/).

You'll need to add Go's bin directories to your `$PATH` environment variable e.g., by adding these lines to your `/etc/profile` (for a system-wide installation) or `$HOME/.profile`:

```
export PATH=$PATH:/usr/local/go/bin
export PATH=$PATH:$GOPATH/bin
```

(If you run into trouble, see the [Go install instructions](https://golang.org/doc/install)).

#### Compile

```
$ export GOPROXY=https://athens.azurefd.net
$ GO111MODULE=on go mod tidy -v

$ go build
```

### Run

1. Create the node configuration file:

```bash
$    go-ibax config
```

2. Generate node keys:

```bash
$    go-ibax generateKeys
```

3. Genereate the first block. If you are creating your own blockchain network. you must use the `--test=true` option. Otherwise you will not be able to create new accounts.

```bash
$    go-ibax generateFirstBlock \
        --test=true
```

4. Initialize the database.

```bash
$    go-ibax initDatabase
```

5.Starting go-ibax.

```bash
$    go-ibax start

https://127.0.0.1:7079/api/v2/getuid
http://127.0.0.1:7079/api/v2/getuid

https://127.0.0.1:8000
http://127.0.0.1:8000


docker build -t ibax/go-ibax -f Dockerfile .

docker build -t ibax/go-ibax-src -f Dockerfile_src .

```





