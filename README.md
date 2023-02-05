# GoReleaser Pro Prebuilt Example

This repo contains a quick and to-the-point example of how to use
[GoReleaser Pro](https://goreleaser.com/pro)
[prebuilt builder](https://goreleaser.com/customization/build/#import-pre-built-binaries).

To run it, clone this repo and run:

```sh
goreleaser release --snapshot --clean -f 1-linux.yml
goreleaser release --snapshot --clean -f 1-darwin.yml
goreleaser release --snapshot --clean -f 1-windows.yml
```

This will create the binaries in `/tmp/dist`.

Next, run:

```sh
goreleaser release --snapshot --clean -f 2.yml
```

This will import the binaries and create archives, nfpm packages, etc.

The `--snapshot` flag is optional in the "real world".
It is required here because it's just an example.
