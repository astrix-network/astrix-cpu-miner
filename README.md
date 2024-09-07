# Astrix-miner

A fast CPU miner for Astrix using AstrixHash algorithm

## How to use the astrix miner

### From Sources

Clone the repo

```sh
git clone https://github.com/astrix-network/astrix-miner
```

Build the miner

```sh
cd astrix-miner

cargo build --release
```

Launch the miner

```sh
cd target/release

./astrix-miner --mining-address astrix:xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```


### From Binaries
The [release page](https://github.com/astrix-network/astrix-miner/releases) includes precompiled binaries for Linux and Windows.


# Usage
To start mining you need to run [astrixd](https://github.com/astrixnet/astrixd) and have an address to send the rewards to.

Help:
```
astrix-miner 0.2.1
A Astrix high performance CPU miner

USAGE:
    astrix-miner [FLAGS] [OPTIONS] --mining-address <mining-address>

FLAGS:
    -d, --debug                   Enable debug logging level
    -h, --help                    Prints help information
        --mine-when-not-synced    Mine even when astrixd says it is not synced, only useful when passing `--allow-submit-
                                  block-when-not-synced` to astrixd  [default: false]
        --testnet                 Use testnet instead of mainnet [default: false]
    -V, --version                 Prints version information

OPTIONS:
        --devfund <devfund-address>            Mine a percentage of the blocks to the Astrix devfund [default: Off]
        --devfund-percent <devfund-percent>    The percentage of blocks to send to the devfund [default: 1]
    -s, --astrixd-address <astrixd-address>      The IP of the astrixd instance [default: 127.0.0.1]
    -a, --mining-address <mining-address>      The Astrix address for the miner reward
    -t, --threads <num-threads>                Amount of miner threads to launch [default: number of logical cpus]
    -p, --port <port>                          Astrixd port [default: Mainnet = 16111, Testnet = 16211]
```


# Devfund
**NOTE: This feature is off by default** <br>
The devfund is a fund managed by the Astrix community in order to fund Astrix development <br>
A miner that wants to mine a percentage into the dev-fund can pass the following flags: <br>
`astrix-miner --mining-address= XXX --devfund=astrix:qqjzemurre653qvkxehfk4x2ngvdnzfusnyr85y8hu04gvq4jcv8q53frrp42` <br>
and can pass `--devfund-precent=XX.YY` to mine only XX.YY% of the blocks into the devfund (passing `--devfund` without specifying a percent will default to 1%)

# Donation Address
`astrix:qqjzemurre653qvkxehfk4x2ngvdnzfusnyr85y8hu04gvq4jcv8q53frrp42`
