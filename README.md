# CosmWasm IBC Address Initializer

 Purpose

This project demonstrates how to achieve cross-chain communication using IBC (Inter-Blockchain Communication) within the CosmWasm ecosystem.  The core concept is a smart contract that can send messages to a replica of itself deployed on a connected blockchain, triggering actions and facilitating a continuous conversation between the instances.

Functionality

** Deployment: The smart contract is deployed on two separate blockchains (Chain A and Chain B).
** IBC Setup: An IBC channel is established between the chains, specifically configured to handle messages for these contract instances.
** Initiation: The contract on Chain A sends an initial message to its counterpart on Chain B.
** Acknowledgment (ACK): Upon receiving the message, the contract on Chain B processes it and dispatches an acknowledgment (ACK) message(address) back to Chain A.
** Replay: The contract on Chain A, within its ACK handler, automatically replays the original message.
