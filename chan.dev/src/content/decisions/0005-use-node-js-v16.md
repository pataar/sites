---
title: "5. Use Node.js v16"
status: "Supercedes [4. Use node.js v18](/decisions/0004-use-node-js-v18.md)"
date: 2023-01-07
---

## Context

Netlify doesn't support node.js v18 🤦

## Decision

Use node.js v16.
Supercede when Netlify (or new host) supports v18.

## Consequences

- Requires that `node-fetch` be used again
  - `node-fetch` has to be pinned to previous major `@2` for module CJS compatability with 11ty
- Netlify `NODE_VERSION` can safely be removed (for now)
- Volta pin needs to be updated to v16
