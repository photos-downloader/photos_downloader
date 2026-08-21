---
title: 状态与路线图
description: 各厂商实现进度，以及文档站、二进制发布的下一步。
---

## 当前

- 文档站已开源：本仓库。
- iCloud CLI：认证、列表、Copy，以及 Sync / Move 相关参数已接通。
- 华为 CLI：基于浏览器 cookie 的云相册下载。
- Xiaomi / vivo / OPPO：脚手架，尚不可用。
- HONOR：接受 cookie，但在 Gallery API 合同验证前不会发真实请求。
- GUI：Flutter + Rust FFI 聚合层存在，安装包未发布。

## 下一步

1. 为已可用 CLI 发布 Windows / Linux / macOS（x64 + arm64）二进制。
2. 把本站下载页接到 GitHub Releases。
3. 完成其余厂商协议后再开放对应指南。
4. 视情况开源各 crate 与 GUI。

## 不会做的事

- 不支持 iCloud Advanced Data Protection（ADP）或 FIDO。
- 不把密码、cookie、session 或带签名的 URL 收进仓库或 issue。
- 不把正在开发的 Flutter Web 调试服务当作官网。
