# Decision log

## 2022-05-05

### No direct exposure of internal API

The internal API (`y-crdt`) is subject to constant changes and does not
necessarily offer an idiomatic Ruby interface. Therefore, the public API of
`y-rb` does not follow the `y-crdt` API, but prefers familiar Ruby idioms when
possible and might even require libraries where it makes sense (e.g. `nokogiri` for XML).

### Rutie is a temporary dependency

The Ruby<->Rust binding feels immature. But it is not the goal of this project
to fix this immediately. The long-term vision is to replace this part by
something more lightweight and opinionated that could be part of the Rust
codebase of this project.