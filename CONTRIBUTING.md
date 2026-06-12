# Contributing to Marmo Desktop

Thanks for your interest in improving Marmo. This guide covers how to get set up and what we expect in a contribution.

## Getting started

1. Fork and clone the repository.
2. Install [Bun](https://bun.sh), [Rust](https://rustup.rs), and the [Tauri prerequisites](https://tauri.app/start/prerequisites/) for your OS.
3. Install dependencies and run the app:

   ```bash
   bun install
   bun run tauri:dev
   ```

## Project layout

- `src/` is the TypeScript interface and wallet logic.
  - `wallet.ts` builds the 2-of-3 wallet and signs transactions.
  - `core.ts` talks to the co-signer service.
- `src-tauri/` is the Rust shell and configuration.

The wallet primitives live in the separate open kit [`@marmoxyz/sui-kit`](https://github.com/marmoxyz/sui-kit). Changes to sharding or signing usually belong there.

## Making changes

- Keep pull requests focused on one thing.
- Match the existing code style. The codebase does not use inline comments.
- Make sure the app builds before opening a pull request:

  ```bash
  bun run build
  bun run tauri:build
  ```

- Describe what you changed and why in the pull request.

## Reporting bugs

Open an issue with steps to reproduce, your platform, and the app version. For anything security related, do not open a public issue. See [SECURITY.md](./SECURITY.md).

## License

By contributing you agree that your contributions are licensed under the [MIT License](./LICENSE).
