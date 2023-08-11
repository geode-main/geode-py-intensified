# Geode Python SDK - INTENSIFIED -

>Geode: [https://www.geode.fi](https://www.geode.fi)
>
>Project Documentation: [https://docs.geode.fi](https://docs.geode.fi)
>
>SDK documentation: [https://sdk.geode.fi](https://sdk.geode.fi)
>
>Source Code: [https://github.com/Geodefi/geode-py](https://github.com/Geodefi/geode-py)

[geodefi](https://github.com/Geodefi/geode-py) is a Python library designed to make things easier for the users of the permissionless [The Staking Library](https://github.com/Geodefi/Portal-Eth)(soon public).

In this repository I will try to cover most of the functionalities for the SDK. Thus, showcasing the possible Node Operation and Pool owner task automations.

> ## Sincerely, WTF is Geode Finance?
>
> Compared to the protocol-oriented DeFi landscape, Geode Finance is the first Decentralized Infrastructure Provider that has developed a unique approach for DeFi and overall smart contract development.
>
> Protocol achieves this by simply distributing packages directly on the blockchain. Users simply customize and initiates an instance of the package. Geode only maintains these packages and releases new versions over time with additional functionalities or security improvements. However, there is no obligation for a user to update their instance of the package. They can simply exist within Geode ecosystem with an older version of the package, without distrupting other instances.
>
> Geode's `The Staking Library` allows any entity to create **their very own staking pool**. Users can customize it according to their needs and have access to many possible functionalities around pooling, staking, delegating and even liquidity management.
>
> `The Staking Library` is also permissonless when it comes to creating a staking pool.
>
> Built on top of this Library, `Operator Marketplace` provides a global standard for the communication between the staking pools and operators. Pools can delegate to their choice of operators and Operators can create validators securely.
>
> You might want to check out our [documentation](https://docs.geode.fi/) for additional information on the protocol.

## Quickstart

### Requirements

`geodefi` (v1.1.1 as of today) requires your python version to be between `3.7` and `3.10`.

### Set up a Virtual Environment

It is suggested to work on a virtual environment:

```shell
sudo pip install virtualenv
python3 -m venv {path}
source {path}/bin/activate
```

### Installation

```shell
python3 -m pip install geodefi
```

### Environment Variables

Here is an example `.env`.

> Note that PRIVATE_KEY is optional.
>
> It is also suggested to change the names for the following variables in your `.env` file, for security concerns.

```env
EXECUTION_API = "https://eth-goerli.g.alchemy.com/v2/xxxx"
CONSENSUS_KEY = "xxxx"
PRIVATE_KEY ="xxxxx" 
```

## Content

- [Getting Started & Important Classes & Utilizing beaconcha.in api](0-Learning-Basics.ipynb)
- [Understanding Portal's Isolated Storage](1-Portal-Isolated-Storage.ipynb)
- [Staking Pools and Beyond](2-Staking-Pools.ipynb)
- [Operators and Operator Marketplace](3-Operator-and-Marketplace.ipynb)
- [Reading available Validator data](4-Validators.ipynb)
- [Sending Transactions through Geode's contracts](5-Sending-Transactions.ipynb)
- [Creating Validators](6-Creating-Validators.ipynb)
- [Example Operator Automation Script](7-Operator-Automation.ipynb)

## Developer Notes

`geodefi` SDK is chain-agnostic, meaning further versions will support other Proof-of-Stake chains that Geode's Staking Library is deployed on.

The library will aslo figure out which chain the user is intending to use this SDK according to provided initialization parameters, such as EXECUTION_API.
