# Web Framework Benchmarks

Benchmarking web frameworks written in [rust] with [rewrk] tool.

More requests(`Req/Sec`) in the given time frame means that framework performs
better.  Which means it would require less (CPU) resources to achieve the same
thing.

`Transfer` in [rewrk] output means received bytes from all of the responses.
Some frameworks include extra headers by default which results in higher count.
This shouldn't impact overall performance much.

## Benchmark Types

### Hello World

Respond "Hello, World!" to every request on "/" endpoint.

- [actix-web v4.5](benchmark/hello-world/actix-web/src/main.rs)
- [axum v0.7](benchmark/hello-world/axum/src/main.rs)
- [hyper v1.2](benchmark/hello-world/hyper/src/main.rs)
- [ntex v1.0](benchmark/hello-world/ntex/src/main.rs)
- [rocket v0.5](benchmark/hello-world/rocket/src/main.rs)
- [tide v0.16](benchmark/hello-world/tide/src/main.rs)
- [warp v0.3](benchmark/hello-world/warp/src/main.rs)

See [results](result/hello-world.md).

[rewrk]: https://github.com/ChillFish8/rewrk
[rust]: https://github.com/rust-lang/rust
