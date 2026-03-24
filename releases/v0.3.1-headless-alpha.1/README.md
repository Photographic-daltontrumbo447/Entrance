# Entrance v0.3.1-headless-alpha.1 发布目录

这个目录承载 `v0.3.1-headless-alpha.1` 这轮公开发布所需的说明材料。

这轮发布是 `V0 HEADLESS ALPHA`。

> English: This directory contains the release materials for `v0.3.1-headless-alpha.1`, which is published as a `V0 HEADLESS ALPHA`.

## 目录里有什么

- `README.md`
- `RELEASE_NOTES.md`
- `GITLAB_RELEASE.md`
- `GITHUB_RELEASE.md`

生成型产物不应进入源码仓：

- zip 安装包
- `SHA256SUMS.txt`
- `package/` 临时目录

> English: This directory keeps release documentation only. Generated artifacts such as zip packages, checksum files, and temporary packaging folders should not be committed to the public source tree.

## 如何重新生成发布物料

### 1. 构建前端

```powershell
pnpm build
```

### 2. 构建 Windows 二进制

```powershell
cargo build --manifest-path .\src-tauri\Cargo.toml --release
```

### 3. 生成 zip 与校验文件

```powershell
powershell -ExecutionPolicy Bypass -File .\releases\package-headless-alpha.ps1
```

### 4. 导出到公开发布镜像仓

```powershell
powershell -ExecutionPolicy Bypass -File .\releases\export-public-snapshot.ps1
```

> English: Rebuild frontend assets, build the release binary, package the headless zip, then export a clean public snapshot before publishing.
