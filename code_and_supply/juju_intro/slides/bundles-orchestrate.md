##  Bundles Orchestrate

```
dockerCluster: 
  services: 
    etcd: 
      charm: "cs:~hazmat/trusty/etcd-6"
      num_units: 1
      to: 
        - 0
    docker: 
      charm: "local:trusty/docker-0"
      num_units: 3
      options: 
        latest: true
    "flannel-docker": 
      charm: "local:trusty/flannel-docker-0"
      num_units: 0
  relations: 
    - - "flannel-docker:network"
      - "docker:network"
    - - "flannel-docker:docker-host"
      - "docker:juju-info"
    - - "flannel-docker:db"
      - "etcd:client"
  series: trusty
```

note:
    Put your speaker notes here.
    You can see them pressing 's'.
