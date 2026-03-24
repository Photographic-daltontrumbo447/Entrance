# GitLab 发布模板

## 标签

`v0.3.1-headless-alpha.1`

## 标题

`Entrance v0.3.1-headless-alpha.1`

## 附件

- `entrance-v0.3.1-headless-alpha.1-windows-x64-headless.zip`
- `SHA256SUMS.txt`

## 描述

直接使用 [RELEASE_NOTES.md](./RELEASE_NOTES.md) 的正文。

> English: Use `RELEASE_NOTES.md` as the release description and upload the zip plus checksum file.

## 步骤

1. 在内部源仓完成代码与文档收口。
2. 运行：

```powershell
pnpm build
cargo build --manifest-path .\src-tauri\Cargo.toml --release
powershell -ExecutionPolicy Bypass -File .\releases\package-headless-alpha.ps1
```

3. 运行：

```powershell
powershell -ExecutionPolicy Bypass -File .\releases\export-public-snapshot.ps1
```

4. 在公开镜像仓确认内容干净。
5. 创建标签 `v0.3.1-headless-alpha.1`。
6. 用同名标题创建 GitLab release，并粘贴 `RELEASE_NOTES.md`。
7. 上传 zip 与 `SHA256SUMS.txt`。

> English: Build, package, export the clean public snapshot, verify it, and create the GitLab release with the same tag and notes.
