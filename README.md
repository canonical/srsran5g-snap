# srsRAN 5G snap

srsRAN is a 5G software radio suite developed by [SRS](https://www.srs.io/).
See the [srsRAN project pages](https://www.srsran.com/) for information, guides
and project news. SrsRAN 5G consists of a combined CU/DU gNodeB that can be used
with real radios or simulated radios over ZeroMQ.

For application features, build instructions and user guides see the
[srsRAN documentation](https://docs.srsran.com/5g/en/latest/).

## Usage

Install and connect the snap:

```bash
sudo snap install srsran5g
sudo snap connect srsran5g:kernel-module-observe
sudo snap connect srsran5g:network-control
sudo snap connect srsran5g:process-control
sudo snap connect srsran5g:system-observe
```

To run the gNodeB, create a configuration file in
`/var/snap/srsran5g/common/gnb.yml` and run the command:

```bash
sudo srsran5g.gnb -c /var/snap/srsran5g/common/gnb.yml
```

Because srsran5g is a confined snap, it can only read and write to its own
directory: `/var/snap/srsran5g/common`.

## Build

To build this snap, you will need a machine with the following requirements:
- Processor: x86-64 dual-core processor
- OS: Ubuntu >= 20.04
- Memory: 8GB RAM

Run
```bash
snapcraft
```
