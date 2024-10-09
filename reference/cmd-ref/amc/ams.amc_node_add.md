## ams.amc node add

Add a node to AMS

### Synopsis

Add a node to AMS.

The new node must have an accessible IP address.

Install LXD on the node before adding it, but do not initialise the LXD instance
with the 'lxd init' command.
AMS takes care of the initialisation and configuration.

```
ams.amc node add <name> <address> [flags]
```

### Examples

```
$ amc node new lxd0 10.48.61.89
nodes:
  - lxd0

```

### Options

```
  -h, --help                     help for add
      --network string           Name of the network device to create on the LXD cluster (default 'amsbr0')
      --network-bridge-mtu int   MTU of the network bridge that is configured for LXD
      --network-subnet string    Network subnet for the network device on the node (default '192.168.100.1/20')
      --storage-device string    Storage device that the LXD node should use
      --storage-pool string      Existing LXD storage pool to use
      --tags string              Comma-separated list of tags to set for the node
      --trust-password string    Trust password for the remote LXD node
      --unmanaged                Expect the node to already be clustered
```

### SEE ALSO

* [ams.amc node](ams.amc_node.md)	 - Manage nodes

###### Auto generated by spf13/cobra on 9-Oct-2024