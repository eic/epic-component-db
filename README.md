# The Component DB


## About

This repository currently serves to describe our findings about, and experimentation with,
the "Component DB" currently deployed for testing purposes by the BNL CAD. It was originally
developed at ANL. We are conducting a feasibility study to determine whether it would meet
the needs of the EIC project and the ePIC Collaboration.

## The Service

A test instance of the database is available at this link:
[https://cdb.eic.bnl.gov](https://cdb.eic.bnl.gov).

## Connecting

User access to the _Web interface_ is limited to ePIC members and needs proper authorization,
please contact ePIC leadership for instruction. Developer access to the database is restricted.
For this purpose, in order to connect from outside of the network perimeter,
one needs to use the _loopback_ connection, after establishing a SSH tunnel for the standard
port on the _localhost_.

```bash
mariadb -h 127.0.0.1 -u root -p
```