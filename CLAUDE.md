# redis-rate-limiter

Redis-based HTTP rate limiter library for Go.

## Build

```bash
make test      # run tests
make clean     # remove vendor/ and dist/
make update    # update dependencies
make release   # create and push a new tag
```

## Test

```bash
go test -v
```

Tests use [miniredis](https://github.com/alicebob/miniredis) for in-memory Redis emulation -- no external Redis instance needed.

## Project Structure

- `limiter.go` -- core rate limiter interface and types
- `counter.go` -- fixed-window counter implementation
- `sorted_set_counter.go` -- sorted-set sliding-window implementation
- `http.go` -- HTTP middleware integration
- `*_test.go` -- corresponding tests
