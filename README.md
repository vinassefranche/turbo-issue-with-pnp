# turbo-issue-with-pnp
Reproducing an issue with turbo@1.7 and pnp

## To reproduce the issue
- run `yarn`
- run `yarn turbo`

See the error:
```
thread 'main' panicked at 'Failed to execute turbo.: Os { code: 2, kind: NotFound, message: "No such file or directory" }', crates/turborepo/src/main.rs:23:10
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
```

## Without yarn plug n play, it works fine
- set `nodeLinker: node-modules` in the file `.yarnrc.yml`
- run `yarn`
- run `yarn turbo`
