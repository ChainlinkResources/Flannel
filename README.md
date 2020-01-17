
# Flannel

> Chainlink oracle extension interface. Working project for Truffle U 2020 enrolment.
> Currently a work in progress, for testnet use only!

## Overview

Flannel is a smart contract which acts a a management interface for a node operators oracle contract. Controlled by function calls from the user's node, Flannel can provide the following features (Work in Progress):

- Withdraw earned LINK from oracle contract at given threshold levels. (Complete)
- Top-up the users node address with ETH - converting withdrawn LINK to ETH via Uniswap. (Complete)
- Option to deposit LINK into the Aave lending pool and earn interest (Awaiting Aave LINK reserve on Ropsten).
- Front-end management interface for configuration (To-Do).

## Getting started

(Detailed instruction to be completed)

1. Set up Chainlink node as per the offical documentation (https://docs.chain.link/docs/node-operator-overview)
2. Deploy Flannel.sol contract using Remix providing addresses of LINK contracts and starting threshold (in wei) at deployment.
3. Transfer ownership of deployed oracle contract to deployed Flannel contract.
4. Create job on Chainlink node using external initiator of choice (example is cron-based) and configure EthTx as based in the example (node_job.json).
5. Wait for Flannel to trigger to see results!


## Test

Local testing currently available for Oracle and Flannel triggering. Clone repo then run:

```
npm install
npm test
```