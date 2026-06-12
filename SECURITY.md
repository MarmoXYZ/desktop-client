# Security Policy

Marmo is a wallet, so we take security seriously and appreciate responsible disclosure.

## Reporting a vulnerability

Please do not open a public issue for security problems.

Email **marmoteam@outlook.com** with:

- a description of the issue and its impact,
- steps to reproduce or a proof of concept,
- the app version, your platform, and any relevant logs.

We will acknowledge your report, keep you updated on progress, and credit you once a fix is released, unless you prefer to stay anonymous.

## Scope

In scope:

- the Marmo desktop client in this repository,
- how it handles shards, signing, and storage of the drive shard.

The wallet primitives live in [`@marmoxyz/sui-kit`](https://github.com/marmoxyz/sui-kit) and the co-signer service is separate. If a report touches those, we will route it to the right place.

## Good to know

- Marmo uses Sui native multisig. The signing threshold is enforced by the Sui network, not by client code.
- The full private key is never assembled in one place. No single shard can move funds.
