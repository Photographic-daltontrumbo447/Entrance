# Entrance v0.3.1-headless-alpha.1

`Entrance` 当前以 `V0 HEADLESS ALPHA` 形式发布。

它是一个以数据库为真相源的连续性运行时，也是一个 headless `NOTA` 宿主。

> English: `Entrance` is currently released as a `V0 HEADLESS ALPHA`: a DB-first continuity runtime and headless `NOTA` host.

## 安装

### 直接使用发布二进制

```powershell
.\entrance.exe nota status
.\entrance.exe nota overview
.\entrance.exe nota checkpoints
```

### 从源码构建

```powershell
pnpm install --frozen-lockfile
pnpm build
cargo build --manifest-path src-tauri/Cargo.toml --release
```

> English: Install from the published binary, or build from source with `pnpm install`, `pnpm build`, and `cargo build --manifest-path src-tauri/Cargo.toml --release`.

## 版权与许可

当前仓库采用收紧的 source-available 许可模式。

- `LICENSE`
- `LICENSES.md`
- `TRADEMARKS.md`

> English: The repository uses a tight source-available license model. See `LICENSE`, `LICENSES.md`, and `TRADEMARKS.md`.
