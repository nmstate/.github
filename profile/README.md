# Nmstate

Nmstate provides a set of  libraries with an accompanying command line tool
that manages host networking settings in a declarative manner. The networking
state is described by a pre-defined schema. Reporting of current state and
changes to it (desired state) both conform to the schema.

Nmstate is aimed to satisfy enterprise needs to manage host networking through
a northbound declarative API and multi provider support on the southbound.
NetworkManager acts as the main provider supported.

Example output:

```yml
$ sudo nmstatectl show
---
dns:
  config:
    server:
      - 192.0.2.1
    search:
      - example.org
routes:
  config:
    - destination: 0.0.0.0/0
      next-hop-interface: eth1
      next-hop-address: 192.0.2.1
interfaces:
  - name: eth1
    type: ethernet
    description: Main-NIC
    state: up
    ipv4:
      enabled: true
      dhcp: false
      address:
        - ip: 192.0.2.9
          prefix-length: 24
    ipv6:
      enabled: false
```

Please refer to <https://nmstate.io/> for more document.


## Contribution

Any pull request is welcome, please reach out these repositories:

 * Rust, Python, C API: <https://github.com/nmstate/nmstate>
 * Documentation: <https://github.com/nmstate/nmstate.github.io>
 * Kubernetes API: <https://github.com/nmstate/kubernetes-nmstate>

For requesting new new repository, please use pull request against
<https://github.com/nmstate/.github/> after below requirements been fulfilled:
 * CI enabled and passed.
 * Has integration test cases proving valid use cases.
 * Licensed under LGPL-2.0+ or Apache-2.0+(preferred).
