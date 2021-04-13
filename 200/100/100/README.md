# 100 - Install faasd with Bash

faasd can be installed with bash. Ubuntu is the preferred OS, but CentOS is also available as an option.
If you don’t have a cloud VM, you can create one with multipass.
The default memory, CPU and disk for multipass is low, but works well with faasd, you can increase it by using
command-line flags. By adding more disk capacity, you can store more container images and functions. In the
advanced section of the eBook there is a script you can use to clean-up old image which are no longer in use.

```
multipass launch --name faasd \
--disk 16G \
--cpus 2 \
--mem 4G
```

Wherever your host is, whether it’s a VM, Raspberry Pi, or cloud instance, you can then install faasd using bash:

```
git clone https://github.com/openfaas/faasd --depth=1
cd faasd
./hack/install.sh
```

Note: this method does not enable TLS, but is the easiest to use for testing. The Terraform installation includes automatic TLS, or you can add it using the instructions in a later chapter.
