##  Charm Anatomy - Metadata

```
name: docker
summary: Deploys Docker Engine, a lightweight runtime and packaging tool.
maintainer: Charles Butler <charles.butler@ubuntu.com>
description: |
 Deploys Docker Engine, a portable, lightweight runtime and packaging tool.
tags:
  - ops
  - application_development
subordinate: false
provides:
  docker-containers:
    interface: containers
requires:
  network:
    interface: overlay-network
```

note:
    Put your speaker notes here.
    You can see them pressing 's'.
