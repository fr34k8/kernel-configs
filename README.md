kernel-configs
==============

A collection of kernel configurations used to build kernels for testing in CKI
project.

The included script, kernel-configs-fetch downloads and outputs a kernel
configuration of the latest kernel for the specified Fedora release and
architecture. Use as such:

    for arch in <arch1> <arch2> .. <archN>; do
        ./kernel-configs-fetch <release> $arch > $arch.config
    done

For example:

    for arch in x86_64 aarch64 ppc64 ppc64le; do
        ./kernel-configs-fetch 28 $arch > $arch.config
    done
