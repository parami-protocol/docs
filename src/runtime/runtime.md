# The Parami Runtime

The Parami Runtime is based on substrate framework, which serves as the foundation for
all AD3.0 functionalities.

Github Repository: <https://github.com/parami-protocol/parami>

Branch for running testnet: `dana-v2`

Development branch: `dana-v3` and `main`

## Pallets

There are some pallets from Parami to implement basic function:

- [did](https://github.com/parami-protocol/parami/blob/main/pallets/did/src/lib.rs) is DID implementation
- [ads](https://github.com/parami-protocol/parami/blob/main/pallets/ads/src/lib.rs) is used for ADs metadata
- [bridge](https://github.com/parami-protocol/parami/blob/main/pallets/bridge/src/lib.rs) is used for bridging to ETH
- [nft](https://github.com/parami-protocol/parami/blob/main/pallets/nft/src/lib.rs) is the ADs NFT
- [token](https://github.com/parami-protocol/parami/blob/dana-v3/pallets/token/src/lib.rs) is the social token for users
- [swap](https://github.com/parami-protocol/parami/blob/dana-v3/pallets/swap/src/lib.rs) is the AMM pallet to swap social tokens


