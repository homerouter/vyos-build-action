# VyOS rolling Fullcone ISO

Builds the current [`vyos/vyos-build@rolling`](https://github.com/vyos/vyos-build/tree/rolling)
ISO with:

- the matching kernel, Intel QAT, and firmware release from
  [`homerouter/vyos-kernel-rolling`](https://github.com/homerouter/vyos-kernel-rolling);
- `libnftnl` 1.3.2-1 from
  [`homerouter/libnftnl-fullcone`](https://github.com/homerouter/libnftnl-fullcone/releases/tag/1.3.2-1);
- `nftables` 1.1.7-1 from
  [`homerouter/nftables-fullcone`](https://github.com/homerouter/nftables-fullcone/releases/tag/1.1.7-1).

The workflow verifies checksums, confirms the exact packages and Fullcone
kernel module are inside the ISO, uploads an Actions artifact, and publishes a
prerelease.

Build the kernel repository first, then run **Build VyOS rolling Fullcone ISO**
from the Actions tab. No repository secrets are required.
