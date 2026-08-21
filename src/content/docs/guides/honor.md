---
title: HONOR
description: 荣耀云相册脚手架会接受 cookie，但在 Gallery API 验证前不会发真实请求。
---

HONOR 提供方目前是脚手架：可以接收浏览器导出的 session cookie，但在用脱敏后的已认证网络轨迹验证 Gallery API 之前，**不会发送真实请求**。

## 安全

不要把以下内容放进 fixtures、issue、PR 或本仓库：

- 密码
- 可复用的 cookie 值
- 账号标识
- 带签名的媒体 URL

协议验证完成前，请把 HONOR 视为不可用。
