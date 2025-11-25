# VecVault

Lightweight local vector embedding store for Node.js supporting in-memory, JSON file, and SQLite backends.

## Features
- Unified API for upsert, query, delete.
- Backends: MemoryStore, JsonStore, SqliteStore.
- Metadata filtering.
- Simple k-NN search with cosine similarity.
- TypeScript support.

## Quickstart

```ts
import { MemoryStore } from "vecvault";

const store = new MemoryStore();

await store.upsert([
  { id: "doc1", vector: [0.11, 0.24], metadata: { tag: "example" } }
]);

const results = await store.query([0.11, 0.24], { k: 3 });

console.log(results);
```

## Backends
- **MemoryStore** — in-memory  
- **JsonStore** — file-based  
- **SqliteStore** — persistent  

## Development
See [CONTRIBUTING.md](CONTRIBUTING.md)

## License
MIT License.
