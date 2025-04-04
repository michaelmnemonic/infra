# infra
Experiements with a kubernetes based infrastructure

1. Download Talos Linux Iso and boot it:
    X86: https://github.com/siderolabs/talos/releases/download/v1.9.2/metal-amd64.iso
    ARM64: https://github.com/siderolabs/talos/releases/download/v1.9.2/metal-arm64.iso

2. Install talosctl

3. Install kubectl

3. Install docker

4. Create the Cluster

```
talosctl gen config <cluster-name> <cluster-endpoint>
```
5. Edit .yaml files

```
talosctl -n 192.168.0.2 get disks --insecure
```

6. Apply config

```
talosctl apply-config --insecure -n 192.168.0.2 --file controlplane.yaml
```
