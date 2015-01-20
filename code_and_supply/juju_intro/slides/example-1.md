##  Example 1


#### Deploy a MySQL Master/Slave replication

```
juju deploy cs:trusty/msyql masterdb
juju deploy cs:trusty/msyql slavedb -n3
juju add-relation masterdb:master slavedb:slave

```

#### Deploy a service that supports read-only replicas

```
juju deploy mediawiki
juju add-relation masterdb:db mediawiki:db
juju add-relation slavedb:db mediawiki:slave
```



note:
    Put your speaker notes here.
    You can see them pressing 's'.
