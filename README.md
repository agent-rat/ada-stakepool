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
For scripts to help the Cardano community please refer to github files

Currently available:
* start_node.sh - Jormungandr startup wrapper script that removes trusted peers that are not reachable (port closed). Originally intended to use nc for port tested by later inspired by ilap's guide to use tcpping - see https://gist.github.com/ilap/54027fe9af0513c2701dc556221198b2
* config/node-config.json - Sample json node-config compatible with start_node.sh
