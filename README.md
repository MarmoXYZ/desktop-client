<div align="center">
  <img src="./public/logo.png" width="96" height="96" alt="Marmo" />
  <h1>Marmo Desktop</h1>
  <p><strong>A self-custody Sui wallet split across three shards.</strong></p>
  <p>Spend with any two of a drive, a non-custodial co-signer, and a recovery login. The full private key never exists in one place.</p>
</div>

---

## What it is

Marmo Desktop is the cross-platform client for the Marmo wallet. It creates a 2-of-3 Sui multisig wallet whose key is split into three shards:

- **Drive** shard, written as an encrypted file to any USB or hard drive you already own.
- **Co-signer** shard, held by the Marmo co-signer service, which can never spend on its own.
- **Recovery** shard, tied to a login for account recovery.

Lose any one shard and the other two still work. Steal any one shard and it is useless alone. Signing is enforced by the Sui network, not by client code, through native multisig.

The wallet logic comes from the open kit [`@marmoxyz/sui-kit`](https://github.com/marmoxyz/sui-kit).

## Download

Grab the latest installer for your platform from the [releases page](https://github.com/marmoxyz/desktop-client/releases/latest):

- macOS: `.dmg` (Apple Silicon and Intel)
- Windows: `.msi`
- Linux: `.AppImage` and `.deb`

## Tech

- [Tauri 2](https://tauri.app) for the cross-platform shell
- TypeScript and Vite for the interface
- [`@marmoxyz/sui-kit`](https://www.npmjs.com/package/@marmoxyz/sui-kit) and [`@mysten/sui`](https://www.npmjs.com/package/@mysten/sui) for Sui

## Develop

Requirements: [Bun](https://bun.sh), [Rust](https://rustup.rs), and the [Tauri system dependencies](https://tauri.app/start/prerequisites/) for your platform.

```bash
bun install
bun run tauri:dev
```

## Build

```bash
bun run tauri:build
```

Installers are written to `src-tauri/target/release/bundle`.

## Contributing

Issues and pull requests are welcome. See [CONTRIBUTING.md](./CONTRIBUTING.md).

## Security

Found a vulnerability? Please report it privately. See [SECURITY.md](./SECURITY.md).

## License

[MIT](./LICENSE)
