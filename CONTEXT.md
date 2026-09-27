# 持久上下文

- 2026-09-28：旧 Vue 项目启动缺少 `vue-cli-service`，原因是尚未安装 `node_modules`。将 JOOX 依赖改为 `vendor/unlock-music-joox-crypto-0.0.1.tgz`，来源为本地 `joox-crypto` 仓库提交 `094ac13`，通过 `npm pack` 打包；依赖安装以 `package-lock.json` 为准。
- 验证：Node 22.14.0 下 `npm ci --include=dev` 成功，`yarn serve` 编译成功且首页 HTTP 请求成功，JOOX 的 4 个测试通过。旧依赖仍存在 Node 引擎声明及样式兼容性警告，当前不影响启动。

- 2026-09-28：已从 `https://git.unlock-music.dev/um/` 下载组织下全部 12 个公开仓库源码 ZIP，目标目录为 `/Volumes/WesternDigitalMbp16/YanQue/Project/Code/Project/um`。下载任务与另一个正在构建 `lib_um_crypto_rust` 的线程完成目录隔离协调。
