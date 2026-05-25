# bASICs VM v3

Thin packaging workspace for the bASICs NixOS VM.

The NixOS build definition lives in the public build repo:

https://github.com/ZimengXiong/basics-vm-nix

This directory should contain only local packaging helpers, cache/output folders,
and a pinned reference to the build repo. The VM image itself should be produced
from the GitHub build repo, not from copied NixOS source in this directory.

## Build from the pinned build repo

```bash
./scripts/build-vm x86_64
```

Outputs are placed under `v3/out/` and ignored by git.

## Refresh the build repo pin

```bash
./scripts/update-build-repo
```

This updates `build-repo.lock` to the current `main` commit of the build repo.
