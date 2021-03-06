# openwrt-packages-umackereld

This is `umackereld` package for OpenWrt, tested on CC(15.05.1).

# How to install binary package

```
$ opkg update
$ opkg install openssl-util
$ echo 'src/gz hnw https://dl.bintray.com/hnw/openwrt-packages/15.05.1/ar71xx' >> /etc/opkg/customfeeds.conf
$ opkg update
$ opkg install umackereld
```

# How to build

To build these packages, add the following line to the feeds.conf in the OpenWrt buildroot:

```
$ echo 'src-git hnw_umackereld https://github.com/hnw/openwrt-packages-umackereld.git' >> feeds.conf
```

Then you can build packages as follows:

```
$ ./scripts/feeds update -a
$ ./scripts/feeds install umackereld
$ make packages/umackereld/compile
```
