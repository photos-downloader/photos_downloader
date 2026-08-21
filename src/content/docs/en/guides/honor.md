---
title: HONOR
description: The HONOR scaffold accepts cookies but will not send live requests until the Gallery API is verified.
---

The HONOR provider is a scaffold: it can accept browser-exported session cookies, but it **will not send live requests** until the Gallery API is verified from a sanitized authenticated network trace.

## Safety

Do not put any of the following in fixtures, issues, PRs, or this repository:

- Passwords
- Reusable cookie values
- Account identifiers
- Signed media URLs

Treat HONOR as unavailable until that verification is done.
