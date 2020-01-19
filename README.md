# AgentRAT ADA-stakepool

## Pool parameters
Fixed : 300
Variable: 2%
Limit: None
Stakepool Id: 5d099136e633d00f53be23c36300f2bfa465fd83f53474dea091042b232b393c

## Current setup
To support the Cardano network, I have setup a testnet ITN node in Melbourne, Australia. The node is hosted on a server

Intel i5 2.6Ghz x 4 core
8Gb RAM 
128 SSD
Optus NBN connection

## Scripts 
For scripts to help the Cardano community please refer to github files. If you like my scripts, just say thanks on Telegram. Nick is [ARAT] AgentRat. Suggestions are also welcomed

### start_node.sh
This is a Jormungandr startup wrapper script. It removes trusted peers that are not reachable (port closed) to speed up the bootstrap process where jorm gets stuck for a long time before moving to the next peer even if the peer's port is not opened. 

Originally intended to use nc for port tested by later inspired by [ilap's guide](https://gist.github.com/ilap/54027fe9af0513c2701dc556221198b2) to use tcpping instead
```
Checking config/node-config.json for trusted peers...
seq 0: no response (timeout)
seq 0: tcp response from ec2-52-28-91-178.eu-central-1.compute.amazonaws.com (52.28.91.178) [closed] 322.049 ms
seq 0: tcp response from ec2-3-125-75-156.eu-central-1.compute.amazonaws.com (3.125.75.156) [closed] 407.774 ms
seq 0: tcp response from ec2-13-114-196-228.ap-northeast-1.compute.amazonaws.com (13.114.196.228) [closed] 153.815 ms
seq 0: tcp response from ec2-52-8-15-52.us-west-1.compute.amazonaws.com (52.8.15.52) [closed] 179.373 ms
seq 0: tcp response from ec2-52-9-132-248.us-west-1.compute.amazonaws.com (52.9.132.248) [open] 179.099 ms
seq 0: tcp response from ec2-3-125-183-71.eu-central-1.compute.amazonaws.com (3.125.183.71) [open] 403.466 ms
seq 0: tcp response from ec2-3-125-31-84.eu-central-1.compute.amazonaws.com (3.125.31.84) [open] 397.943 ms
seq 0: no response (timeout)
seq 0: tcp response from ec2-54-183-149-167.us-west-1.compute.amazonaws.com (54.183.149.167) [open] 178.491 ms

Regenerating config/node-config-runtime.json...

Launching jormungandr...
bin/jormungandr --genesis-block-hash=8e4d2a343f3dcf9330ad9035b3e8d168e6728904262f2c434a4f8f934ec7b676 --config config/node-config-runtime.json --secret config/node-secret.yaml
{"msg":"Starting jormungandr 0.8.5 (master-33c8d985, release, linux [x86_64]) - [rustc 1.40.0 (73528e339 2019-12-16)]","level":"INFO","ts":"2020-01-19T13:17:04.736653938+00:00","task":"init"}
```

Sample json node-config at config/node-config.json

