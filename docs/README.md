# SafExpr Documentation

SafExpr is a **safe, minimal, and type-safe expression engine** for JavaScript and TypeScript.

Use it when you need **formulas, filters, and business rules** without `eval`, without global access, and with a TypeScript-friendly API.

## What you will find here

- [Overview](./overview.md) — architecture, design goals, and the safety model at a glance.
- [Getting Started](./getting-started.md) — install the package and run the first expressions.
- [API / `compile`](./api/compile.md) — one-off expression compilation.
- [API / `createEngine`](./api/engine.md) — reusable engines with helper functions.
- [API / Plugins](./api/plugins.md) — plugin patterns and extension points.
- [Expression Syntax](./guides/expressions-syntax.md) — supported language features.
- [Migration Guide](./guides/migration-guide.md) — move from `eval`, custom DSLs, or other engines.
- [Security Model](./guides/security-model.md) — sandbox boundaries, threat model, and safe usage.
- [Examples](./examples.md) — ready-to-copy usage patterns.

## Recommended reading order

1. [Overview](./overview.md)
2. [Getting Started](./getting-started.md)
3. [Expression Syntax](./guides/expressions-syntax.md)
4. [API / `compile`](./api/compile.md)
5. [API / `createEngine`](./api/engine.md)
6. [Security Model](./guides/security-model.md)
7. [Examples](./examples.md)

## Quick start

```ts
import { compile } from 'safexpr';

type Context = {
  price: number;
  qty: number;
};

const expr = compile<Context, number>('price * qty');
const total = expr.eval({ price: 19.99, qty: 3 });
```

Continue with [Getting Started](./getting-started.md).
