# Changelog

## Version 1.0.0

Firmware:
d17f34e113 config: set BUILD_TYPE=release
20e25c82d6 Makefile: do not include git-revision in filename of releases
524bf974ec Makefile: update release-hack
37c884dfa6 Makefile: workaround to allow releasing
e6a44da8f3 Makefile: detect if we running on a special host
708240926d Makefile: prefix images with "hedy"
024ba575ad config: set Release-Name "Hedy-1.0.0"
caa7958715 packages: remove "migration" for Hedy-1.0.0
1ea456fcf8 config: set VERSION to Hedy-1.0.0-rc
23de946c74 config: explicitly add options regarding version-info in filenames
ec06e30ea4 Makefile: add setting "SET_BUILDBOT"
cad82aea78 Makefile: add BUILD env "IS_BUILDBOT"
4ff2c2d631 Merge branch 'packages/notunnel'
64cd8de4b1 patches: do not run policy-routing script on interface ffuplink
c81f697d9a Revert "profiles: disable all 4MB-targets"
ba3cb3f41e netifd: update to git HEAD version (2017-03-07)
5550d6bb52 configs: add package ffuplink-notunnel
3800686f94 configs: add kmod_veth
92ccc54e86 packages: create empty list for 4MB-targets of vpn03, tunnel_berlin
da52348b99 packages: change "default" as notunnel-setup
f6feba5841 packages: add variant for uplink w/o tunnel
c45b9b6055 update packages-berlin to HEAD (2 Feb 2018)
cd1f5bfa2f update OpenWRT-routing to lede-17.01 HEAD (2 Feb 2018)
7183bc6c38 update LuCI-feed to HEAD of lede-17.01-branch (2 Feb 2018)
81e9f5dda4 update OpenWRT-packages to HEAD of lede-17.01 branch (2 Feb 2018)
0b7aa08806 Add "diffutils" and "patch" to optional packages
d3c50b6d67 hostapd: disable 802.11 legacy-rates by default
618a9e138f Revert "patches: add "fix-meshid" for ieee802.11s"
567f31c0e4 update LuCI-feed to HEAD of lede-17.01-branch (23 Jan 2018)
11ad3307a3 update OpenWRT-packages to HEAD of lede-17.01 branch (23 Jan 2018)
916c71d200 update OpenWRT-routing to lede-17.01 HEAD (15 Jan 2018)
47db7e2934 update to HEAD of LEDE-17.01 (22 Jan 2018)
3a11623858 switch to primary OpenWRT Repo-URL
613b84d215 Revert "add support for LEDE" to follow remerge with OpenWRT
97b86bec79 update to HEAD of LEDE-17.01 (30 Dec 2017)
696871104f Add Raspberry Pi 3 configuration
d84f5f2b52 update to HEAD of LEDE-17.01 (16 Dec 2017)
de04c020e7 feeds: update OpenWRT-routing to lede-17.01 HEAD (Dec 7, 2017)
c8365bdfa1 feeds: update LuCI-feed to HEAD of lede-17.01-branch (Dec 2, 2017)
823d2af23e feeds: update openwrt-packages to HEAD of lede-17.01 branch (Dec 2, 2017)
72df4e4b0f update to HEAD of LEDE-17.01 (8 Dec 2017)
7e68b61228 RaspberryPi: fix wrong filenames and profile-name
7251b6648f added RaspberryPi configuration
398aee0684 configs: in preinit and failsafe change network to 192.168.42.1/24
1b45bfce15 patches: use olsrd v0.9.0.3
8a5f046e1a patches: change etc/openwrt_release to contain build-revision
07e9d690e4 config: update to HEAD of LEDE-17.01 (Oct 25, 2017)
061f489a32 patches: add "fix-meshid" for ieee802.11s
a33755ecf3 feeds: update packages-berlin to HEAD (Oct 29, 2017)
a0d1ca0ecd backport Ubiquiti ERX SFP to LEDE 17.01
749d462358 patches: fix 3cf833c
8cfc6fadab feeds: update LuCI-feed to HEAD of lede-17.01-branch (Oct 18, 2017)
2cb53c096c feeds: update openwrt-packages to HEAD of lede-17.01 branch (Oct 16, 2017)
3cf833ccd0 config: update LEDE to HEAD of 17.01-branch (Oct 18, 2017)
590a07ef19 profiles: remove GL.iNet GL-MT750
37636086a5 patches: fix Xen-x86-domU + serial-console
d615ce1ab7 packages: cosmetic-change - reorder list of packages
d7dca87377 adapt to new packages for VPN03 and tunnel-berlin
7739d59bfe config: update to HEAD of LEDE-17.01 branch (3. Oct 2017)
c1dca95efa feeds: update to HEAD of Packages/LuCI/Routing feeds (3. Oct 2017)
65467d3986 feeds: update packages_berlin
e6e70c28f8 feeds: update OpenWRT-LuCI to lede-17.01 HEAD (Aug 20, 2017)
5580afcf27 feeds: update OpenWRT-routing to lede-17.01 HEAD (Jul 10, 2017)
07bcbefd9c feeds: update OpenWRT-packages to lede-17.01 HEAD (Sep 15, 2017)
950b7ff3a8 config: update LEDE 17.01 to HEAD (Sep 14, 2017)
972e689370 assemble_firmware: skip usecases with empty package-list
75d328eac3 assemble_firmware: fix usage of space / tab
9e7deaf193 config: update to LEDE 17.01 HEAD (Aug 17, 2017)
6d79975cf0 feeds: update berlin-packages (Aug 28, 2017)
71238c9edb feeds: update openwrt-luci to lede-17.01-HEAD (Aug 7, 2017)
c3996fc4c1 feeds: update openwrt-packages to lede-17.01-HEAD (Aug 13, 2017)
3aaaf158fe feeds: update berlin packages to HEAD (Aug 16, 2017)
79b97eefb6 Merge pull request #473 from freifunk-berlin/add-libustream-mbedtls-to-default-backbone-image
60aec8d86e config: fix "update to LEDE-17.01 HEAD (Tue, 25 Jul 2017)"
3dd9eaf575 Allow ICMP for busybox traceroute
cf1fa38dc2 config: update to LEDE-17.01 HEAD (Tue, 25 Jul 2017)
8f5085c6f6 configs: build kmod-nf-nathelper-extra as module
789cb17c6a packages: add libustream-mbedtls to default and backbone package set
cdfd3b0b5e add packages to support ipip-tunnels
bf1c877c91 update berlin-packages (Jun 24, 2017)
4bfe948e6b feeds: update routing, LuCI, packages
80ef4feadf update LEDE to 17.01 HEAD (Wed, 28 Jun 2017)
f75f5a9439 config: update LEDE to V17.01.2 (Sat, 10 Jun 2017)
67d14775c6 configs: add i2c and gpio modules for ramips-mt7621
9ab17688e2 Makefile: fix dependencies when patching LEDE
a386a2d78e configs: remove explicitly selected i2c-stuff
0ce68fcba0 profiles: add ubnt-erx-sfp for ramips-mt7621
4176688fc3 patches: add Ubiquiti EdgeRouter X-SFP (UBNT-ERX-SFP) support
35e8419d27 packages: add tcpdump to the default package set
db47a2d24e assemble_firmware: workaround for failing imagebuilder when "BIN_DIR" is defined
f8dc9aa640 profiles: add TP-Link WR1043ND-v4
8765a27ee5 added some buffalo ar71xx targets
023850a219 Readme: note about target images usage
97eef0a600 Makefile: new target images to only create the firmware-images
f2add41295 feeds: update berlin-packages
436df00f78 config: update LEDE-17.01 HEAD
8f58766564 feeds: update openwrt-packages and openwrt-luci
072459ea88 config: update LEDE to 17.01-HEAD
fa11c670b6 profiles: enable TPLink Archer C5 V1
9c75627e0b Merge pull request #461 from SvenRoederer/add_some_packages
ac6dd7c412 configs: add iperf3 and collectd-modules conntrack, irq
d02b09ff62 configs: add PPPoE-support
c78ade1737 Merge pull request #453 from freifunk-berlin/improve_Makefile
4c44264d35 Merge pull request #456 from freifunk-berlin/deprecate_6to4
6621d89260 README: add TARGET ramips-mt7621
cb7789cc8d feeds: update packages (fix issue #454)
5555359d08 feeds: update packages
0ad2405352 feeds: update LuCI
13beb2fe02 README.md: update TARGETs to new full syntax
64dfaea367 Makefile: move files instead of copy
d4465bb36f Makefile: add rule .stamp-images
9a331fb011 configs: remove deprecated 6to4-package
70629c31d3 Makefile: test for existing $TARGET-config
f61ddcc3de Makefile: change updating of feeds to single commands
4c07e3abce Makefile: also remove sdk and imagebuilder from builddir on clean-target
eb1767c9b6 Merge branch 'issue_432'
2749a36a02 feeds: update LuCI
58f92e33e5 feeds: update packages
543f85632e config,feeds: update LEDE, packages and LuCI
99ce8de2ae README, CHANGELOG: update for Kathleen 0.3.0
6606e57cd0 config.mk: update to LEDE v17.01.1
2f725a2b95 feeds: update berlin-packages
9264040e57 feeds: update LuCI
c2bc113f81 feeds: update packages
a2bee31513 config,feeds: update LEDE, packages and LuCI
45e50734e5 Revert "profiles: disable GLinet MT300a"
86330521ff Makefile: IB_BUILD_DIR is obsoleted by assemble_firmware.sh
cdc1404263 Makefile: remove unused TOOLCHAIN_PATH
86e155c2df configs: select collectd-dhcp-addon by default
fb8557bf01 feeds: update berlin-packages
5de5f99206 profiles: disable GLinet MT300a
9a63e55e1c configs: set release to Hedy 1.0.0-alpha
e7b8a364d5 Makefile: define separate target for VERSION.txt
38d96a486e assemble_firmware: check for usecase-file
75933e3c93 configs: remove faulty tab
eab03437c4 config, feeds: update to LEDE 17.01.0 release
be2a7879a9 Makefile: use "$(MAINTARGET)-$(SUBTARGET)" instead of $(TARGET)
105d293ef9 assemble_firmware: check for files in embedded-directory
ef11714b86 Makefile: fix embedded-files/
de96d19c73 patches/banner: update to new version number handling
c2573c9973 embedded-files: Revert embedding banner-file
274cd8131a add arch ramips-mt7621 to build for EdgeRouter X
d1d7755eaf profiles: add GL-Inet GL-MT300A, GL-MT300N, GL-MT750
28db5dd06c Merge pull request #420 from freifunk-berlin/SAm0815/build_with_lede
7cd6280bb1 Makefile: update renaming to new imagenames
2fb40b2061 Makefile: put revision-hash in CONFIG_VERSION_CODE
827d03c43e profiles: disable all 4MB-targets
785c9bde58 configs, packages: use OpenVPN-openssl for RSA1024-keys
048493a6fa configs, packages: libpolarssl has been replaced by libmbedtls
b8292dec06 configs, packages: uhttpd-mod-tls has been removed
f9de53e543 configs/common: use px5g-polarssl instead of deprecated px5g
d65f5fa17b configs: enable telnet client
d2f4aa74bb configs: disable "HORST", which fails to build
282c926c79 remove kmod-ipv6
a05e97b6ac profiles: update profiles to board names
3328677ef0 Makefile: handle non-existing imagebuilder, sdk or toolchain
74ca01da94 Makefile: use xz for imagebuilder and sdk
7cc815a20d Makefile: correct package copy into the new lede structure
d888c21df6 add support for LEDE
ebe7cf9bff assemble-firmware: add parameter "-e"
a66896d3ca Makefile: use openwrt/files to embedd files directly into image

packages:

## Version 0.3.0

* OpenWrt ChaosCalmer of Mar 09, 2017 (9a1fd3e)
  * kernel 3.18.45
* OpenWrt packages of Apr 8, 2017 (b5f4718)
* OpenWrt LuCI of Jan 13, 2017 (b89b022)
* Berlin-packages of Apr 9, 2017 (6bd5486)

### packages
```
dhcp-defaults: quieten dnsmasq
collectd-addons/dnsmasq: package added
```

### hardware-support
```
build GL.inet AR300, MT300a, MT300n
build Buffalo WZRHPG300NH2, WZRHPAG300H, WZR600DHP, WZRHPG450H
build TPlink-WR941
```

### build
Makefile is compatible to the current LEDE-compatible 
```
convert target-names to include always MAINTARGET and SUBTARGET
Makefile: split off firmware assemble from Makefile
append subtarget name to all platforms
```

## Version 0.2.0

* OpenWrt ChaosCalmer of Nov 8, 2016 (1b6dc2e)
  * kernel 3.18.44
  * improved Security, hardware-support
  * fixes bricking NanoStations XM with original-firmware >5.5
* OpenWrt packages of Oct 29, 2016 (e3e9f34)
  * Collectd V5.4.2
* OpenWrt LuCI of Nov 8, 2016 (9047456)
* OpenWrt routing of Jun 7, 2016 (d580d71)
  * olsr v0.9.0.3
  * batman-adv: 2016.1 bugfixes & stability updates
  * OONF release 0.12.1

### packages
```
patches: fix issue#402 (bypass VPN on mesh)
snmp-templates: add template to query Ubiquiti AirMax via SNMP
configs: add package snmp-utils
configs: do not build ffwizard-pberg
[packages] use luci-mod-freifunk-ui
enable CONFIG_PACKAGE_kmod-ppp for PPPoE/PPP/mobile connections
[luci-app-ffwizard-berlin] do not use ffwatchd
packages/default_4MB: remove opkg and usign
build kernel modules for usb-ethernet tethering
[packages]: build luci-app-olsr-viz as package
[configs] build kernel modules for cifs/ext4/vfat, nls, USB ACM/serial/storage
[configs] build luci-app-splash
[configs] build olsrd2
remove l2gvpn package
remove libwebsocket and websocket server implementation
remove auto-ipv6-node package
remove auto-ipv6-gw package
remove ffwizard-pberg
remove luci-app-chat
```

### hardware-support
```
add OpenWRT-support for TP-link WR-842v3
OpenWRT added support for TPlink WR841-v11 and others
add TP-link MR3220 for ar71xx
add GL.inet AR150, AR300, DominioPi, MT300A+N, MT750
add GL-AR150 support
add support for D-Link DIR505 router
Add profile for TP-Link TL-WA801N/ND routers.
add version 1.1 support to CPE210/220/510/520
Add support for Archer C7 v2
add ramips config (Nexx WT3020)
add GL.iNet 6416A
```

### feeds
```
[patches] update OWM API URL
[olsrd-defaults] fix filename of olsr6 watchdog file
network-defaults: add workaround for too high txpower on NanoStation M2
[ffwizard] fix replacing VPN key/cert
fork freifunk-ui from luci-mod-freifunk-ui
[ffwizard] set start and limit in dhcp configuration
[freifunk-berlin-openvpn-files] start OpenVPN via hotplug script, use --local for binding to WAN IP only
Replace dyngw ping check target with stable ones
[ffwizard] remove all references to uci "system.system.latlon"
[ff-berlin-statistics-defaults]: change ping host for collectd
[ffwizard] [migration] use ffvpn for QoS rather than wan
[uhttpd-defaults]: do not force a redirect to https
[owm] add --dry-run option for debugging
```

### config
```
[configs] disable kernel Swap-support
[configs] use LUCI_SRCDIET=y to create smaller rootfs
[configs] disable SSP_SUPPORT
[configs] strip kernel exports
```

### build
```
patches: add PATCHES.rst to introduce a counting structure
Makefile: add target openwrt-clean-bin
Makefile: add unpatch target
[patches] run postinst-script just before building the image
split up configs into common part and arch-specific part
Makefile: create VERSION file with git branch and revision
Set VERSION and REVISION string from this firmware repository
```

## Version 0.1.2

```
[patches] update OLSRd to v0.9.0.2
[feeds] update firmware-packages (OpenVPN mssfix)
```

## Version 0.1.1

* https://github.com/freifunk-berlin/firmware/commits/v0.1.1
* https://github.com/freifunk-berlin/firmware-packages/commits/v0.1.1

## Version 0.1.0

### packages

```
[packages] add basic packages list for backbone nodes (83c5fb3)
[packages] add luci-app-firewall (d6d26f6)
[packages] bbb - add tcpdump (89e14bd)
[packages] build and integrate freifunk-berlin-migration package into firmware (55b9fe5)
[packages] rename lists to 'default' and 'minimal' (8bf3979)
```

### config

```
config.mk: Update OpenWrt revision to 44162 (4fb186f)
[configs] build ath{5,9,10}k wifi drivers as modules for x86 target (5dab54c)
[configs] build tcpdump as optional package (5d6b47a)
[configs] increase VERSION_NUMBER to 0.1.0 (baeed92)
[configs] update default packages list (848bc23)

```

### feeds

```
[feeds] change url for packages berlin to new repo url (dbf79a8)
[feeds] update feeds to include vpn03-firewall fix (a72f5de)
[feeds] update packages berlin (0e62c8f)
[feeds] update packages_berlin (8b524d0)
[feeds] update packages_berlin feed (363e526)
[feeds] update packages_berlin feed (fc2e535)
[feeds] update routing feed (5a46b41)
[feeds] update routing feed (a1018bb)
[feeds] update routing feed (b98f5f2)
```

### patches

```
[patches] add two ipv6 nameservers (83df6ab)
[patches] backport support for ubnt loco xw (7142d00)
[patches] change default dhcp leasetime to 5 minutes (b38af12)
[patches] fix ascii art in /etc/banner (99a4382)
[patches] fix ascii art in /etc/banner (9c8394c)
[patches] fix firstboot checkpasswd condition (6c943d9)
[patches] fix redirect on firstboot (8dc3728)
[patches] fix regression introduced by openvpn update in openwrt release (08762ad)
[patches] remove 008-luci-freifunk-gwcheck.patch (5328184)
[patches] remove dead code and add a comment (afaef84)
[patches] remove olsrd PingCmd patch (now in upstream release) (1cfb3e6)
[patches] remove the PingCmd patch from series file (3f66f8c)
[patches] remove unused regdb.txt patch (ec39bf0)
```

### build

```
[profiles] add support for TL-WR710N (6ac7e57)
[Makefile] fix wrong directory for packages (613875b)
[Makefile] new firmware directory layout (e40935f)
[Makefile] only copy imagebuilder once for each target (1260cda)
[Makefile/Packages] rename minimal to backbone (c2413e2)
[Makefile] Support for different packages lists (066e80e)
remove 4MB constraint from mikrotik profile (74e8316)
update openwrt/packages to head of branch for-14.07 (9b2c15c)
```

### misc

```
CHANGELOG.md: fix version number (a309bbf)
CHANGELOG.md: Fix markdown for CHANGELOG.md (9b0693b)
fix multiple policyrouting rules (9a72280)
fix policyrouting typo (208aada)
[README] add firmware directory layout (9ca1762)
[README] add ipv6 resolvers to feature list (811566d)
[README] fix imagebuilder location (847302e)
[README] mention some prerequisites for the build process and add some links (cba0a89)
[README] some restructuring; buildbot/branch notes; news part I (06abf0f)
```

## Version 0.0.0

### Packages

```
[packages] added luci-app-openvpn (092822a)
[packages] Add batctl to list (86de22f)
[packages] add collectd-mod-uptime and -mod-memory (32962c8)
[packages] added alfred to package list (337c54c)
[packages] added mtr to minimal list (35ade53)
[packages] add freifunk-berlin-firewall-defaults (e474626)
[packages] add freifunk-berlin-statistics-defaults (3731064)
[packages] add olsrd-mod-txtinfo (7e627e4)
[packages] add olsrd-mod-txtinfo and olsrd-mod-dyn-gw (f59e432)
[packages] move default values for olsr and network in own packages (bfe776d)
[packages] add px5g (4e8680a)
[packages] refactoring and removing unnecessary entries (ec94dc8)
[packages] refactor packages (80413ae)
[packages] remove 6to4 (61bcec0)
[packages] remove duplicate olsrd-mod-jsoninfo package (8ac0530)
[packages] remove wpad package (a845e14)
[packages] remove wpad (pulled in by mpc85xx) (0e6b5b6)
[packages] remove alfred from ar71xx.config (488f240)
[packages] remove auto-ipv6-{gw,node} from ar71xx.config (7a0d190)
[packages] remove olsrd-plugin-txtinfo (fix #103) (b01b4ca)
[packages] rename package list 'minimal' to 'vpn' (f42dc9c)
[packages] replace ar71xx.config with sane new config (130b8e1)
[packages] Add default packages for dhcp and freifunk (646e295)
[packages] Added additional packages to configs (227c13d)
[packages] Added freifunk-berlin-openvpn-files and freifunk-policyrouting (77fcddc)
[packages] Added package tmux to configs (0efc3ca)
[packages] Adding python to the list of missing pakages. (Missing for docker ubuntu images) (15cd128)
```

### Config

```
[configs] Added rudimentary packages list (024cafb)
[configs] #7 added luci-app-firewall package (c4db051)
[configs] do not use IGNOE_ERRORS=m (ced9337)
[configs] update openwrt revision (latest change) (e6abd81)
[configs] update openwrt revision to latest revision (4a6fcbb)
[configs] add community-profiles to ar71xx.config (2090804)
[configs] added alfred as package fixed dyn_gw (9f6e774)
[configs] added mtr as package to build (684647a)
[configs] add freifunk-berlin-firewall-default package (e949442)
[configs] add lib-guard, statistics-default and olsrd-mod-txtinfo (ee367b8)
[configs] add om-watchdog for OM2P target (1ec3938)
[configs] add px5g (00d8cc5)
[configs] add px5g to ar71xx.config (402ec38)
[configs] add x86 as target (42ca4df)
[configs] build with SSP_SUPPORT/libssp (d88f13c)
[configs] enable DFS support in ar71xx.config (1541177)
[configs] fix #20 VERSIONOPT bug (484d68a)
[configs] honor users regdb configuration (3b609e4)
[configs] only build image builder for ar71xx (83dc48b)
[configs] remove ppp support and some kernel debug flags (268812b)
[configs] set version information (622576d)
[configs] strip polarssl (aa81db0)
[configs] update repo link to buildbot (8e685fd)
[configs] update routing and luci (8b9a534)
[configs] update ar71xx (3229ebe)
[configs] fix https duplicated commonname/issuer id problem (e703655)
[configs] use barrier breaker 14.07 branch (92a31ed)
[configs] Add minimal package lists for 4MB flash devices (09bf78c)
[configs] add OM2P boards to ar71xx profiles (fbacfc5)
[configs] Add support for different default packages list (92f8ba9)
[configs] Add target 'x86' (aea021f)
[configs] update ar71xx.config to current openwrt revision (92a310e)
[configs] update luci feed and remove obsolete map patch (d0d4284)
[configs] Update OpenWRT version (e5737d7)
```

### Feeds

```
[feeds] packages_berlin ffwizard added qos script (fb78ccd)
[feeds] packages_berlin ffwizard set mac addr if present (4e3f5e9)
[feeds] packages_berlin firewalldefaults Add unreachable rules for tunl0 (f7fb9a0)
[feeds] update routing feeds (9877987)
[feeds] packages_berlin olsrddefauls ipv6 stuff (15e7724)
[feeds] update olsrd to 0.6.7.1 (66dfd72)
[feeds] update luci feed (3b4e592)
[feeds] adapt feeds for freifunk (e4ef5a6)
[feeds] add support for statistics (e1d5f4b)
[feeds] bugfixes for ffwizard and freifunk-defaults  freifunk-defaults - add missing firewall rules  ffwizard-berlin - set wan type to bridge for private APs (63d7cdf)
[feeds] change page order of optional stuff and wireless (a31ed55)
[feeds] configure olsrd with defaults values from community_profile (ce2ffed)
[feeds] update luci feed and rebase/remove patches (087fc30)
[feeds] update revision of packages-berlin remove defaults from wizard (e714ddd1)
[feeds] ffwizard - activate dhcpv6+ra server mode for odhcpd for dhcp network (787b311)
[feeds] ffwizard-berlin: firewall - add dhcp to freifunk zone (95f4a51)
[feeds] ffwizard-berlin - only configure statistics if installed (8963389)
[feeds] ffwizard-berlin support wifi iface5, osm tiles (9f6c437)
[feeds] ffwizard-berlin - use HT40 only for channels 36..100 (2e353a9)
[feeds] fix copy/paste error in uci-defaults of ffwizard-berlin (9bf4324)
[feeds] fix zoom level for map in ffwizard-berlin (0696a93)
[feeds] olsrd defaults - add RtTablePriority to fix netlink errors (9f057b3)
[feeds] pin down all feeds to a specific commit (886ccf9)
[feeds] update berlin-packages always enable policy routing (65e57cb)
[feeds] update berlin-packages ix openwifimap, wireless ap config (57a8c1b)
[feeds] update berlin-packages update for smartgw and dyngw (470aea0)
[feeds] updated packages_berlin add lib guard fix ipinfo (af6aa36)
[feeds] update ffwizard-berlin fix countryCode,olsr, qos (821a29f)
[feeds] update ffwizard-berlin wizard with map, private ap, vap (7e2652b)
[feeds] update luci feed (3b4e592)
[feeds] update package_berlin (9919dd4)
[feeds] update package_berlin change default ip to 192.168.42.1, add static
[feeds] update package_berlin remove p2pblock, added switch-ports to br-dhcp (ff83bd4)
[feeds] update packages-berlin no ipip tunnel if uplink (e336804)
[feeds] update packages_berlin update openvpn setup (b79c5d4)
[feeds] update packages_berlin toggle stats in wizard (c9d419f)
[feeds] use dyngw instead of dyngw_plain+ff_olsr_gwcheck (ec593c6)
[feeds] use ffwizard-berlin (1580033)
```

### Patches

```
[patches] update olsrd dynamic gw ping cmd patch (8f90f36)
[patches] remove olsrd ipv6 bind only patch (366ea66)
[patches] add fix for mac address issues for wdr4900 (4fd9c3f)
[patches] firstboot - fix auth parameters (734e95e)
[patches] pr - add rule for tunl0 to olsr-tunnel (b0901b9)
[patches] #18 redirect to ffwizard without login (5732ad5)
[patches] #18 redirect to freifunk wizard on first boot (3085cc6)
[patches] #41 change ssid to berlin.freifunk.net (5d4f9e1)
[patches] add barrier breaker patches (38aa6b7)
[patches] add bind ipv6 only patch for olsrd txtinfo and jsoninfo (6cb7a33)
[patches] add default values for olsrd to community_profile (90e8e97)
[patches] added freifunk gwcheck jshn patch (ac0327a)
[patches] Add Freifunk to /etc/banner (fcc948b)
[patches] add patch for hostapd dfs (2e1297e)
[patches] add '%' to valid olsrd option values (7e14e99)
[patches] adjust to new ffwizard config (d55358e)
[patches] firstboot - only set username/password in url if password is blank (24ada56)
[patches] fix #79 - invalid autogenerated olsrd config (fd4638c)
[patches] fix name of freifunk-policyrouting-hotplug-device patch (323941b)
[patches] fix paths of jshn-patch (8a8ec63)
[patches] import luci-freifunk-gwcheck.patch (005aabe)
[patches] import luci-freifunk-map.patch (75ced53)
[patches] import luci-freifunk-policyrouting-berlin.patch (0c748b6)
[patches] import luci-mod-admin-dfs.patch (08f5ed0)
[patches] import luci-olsr-controller.patch (c508d1a)
[patches] incorporate fixes for olsrd dynamic gateway ping command patch (5592edb)
[patches] merge profile berlin patches (563c955)
[patches] olsrd - add dyn gw PingCmd param (66cc0a8)
[patches] profile_berlin - add country and mcast_rate (e90753e)
[patches] profile_berlin - add wifi_device and _iface for 5GHz (5823e89)
[patches] redirect only if no password is set (fec200b)
[patches] remove 002-target-atheros-whr-hp-ag108-sysupgrade.patch (28f5d22)
[patches] remove 003-comgt-dep-ppp.patch (a1d895c)
[patches] remove 004-package-openssl-broken.patch (802e72b)
[patches] remove 006-target-imagebuilder-remove-initramfs-dep.patch (d7cf86f)
[patches] removed dfs related patch which breaks /sbin/wifi (d5b1e73)
[patches] remove !initramfs dependency of imagebuilder (ae80af8)
[patches] remove non existent freifunk community profiles (6c49443)
[patches] remove obsolete olsr defaults (4558f8c)
[patches] remove owm_api and mapserver key from community profile (d4ee2e1)
[patches] remove redundant country param in profile_berlin (0185677)
[patches] remove RtTableTunnel for olsrd6 (a0cb0ea)
[patches] rename 007-routing-olsrd-ipv6-bind-only.patch (9abde9d)
[patches] rename dev to DEVICE in freifunk-policyrouting hotplug script (96007ff)
[patches] set netmask for interfaces to 255.255.255.255 (c0d736b)
[patches] use intern-chXX.freifunk.net as ssid scheme for adhoc (6ce8f59)
[patches] use luci.model.ipkg instead of luci.fs to check if wizard is installed (4a0e6a7)
```

### Build

```
[Makefile] add images target (1ea1da7)
[makefile] add MAKE_ARGS (8aaf7ce)
[Makefile] add pre-patch target (3f4fe00)
[makefile] compile and build firmwares by default (60a0218)
[makefile] use diffconfigs (1f90d9b)
[makefile] do not execute imagebuilder manually (bc51253)
[makefile] fix parallel issues (653ade2)
[makefile] fix patches symlink (70f014f)
[Makefile] fix possible issue with imagebuilder (979539a)
[Makefile] fix quilt dir (48af529)
[Makefile] quilt from openwrt toolchain for patching (9d259a7)
[makefile] images target -> firmware target (7df4262)
[Makefile] inject config after patches have been applied (3aa788b)
[Makefile] let make clean invoke ./scripts/feeds clean (fa2f1ad)
[makefile] moarrr profile fixes (361de16)
[Makefile] place binaries in expanded target dir (with subtarget) (7f1eb98)
[makefile] revamp makefile with stamp files (0b314b6)
[Makefile] set SHELL to bash (471c0f1)
[Makefile] set umask to 022 (c8d46aa)
[makefile] support multiple profiles (7e28bd1)
[makefile] support subtargets (178ff19)
[makefile] add configurable make command MAKE_CMD (a8a8ad1)
[makefile] also remove repositories with git clean (4f2cd3e)
[makefile] apply patches w/ quilt (d80f181)
[makefile] fix PWD (13a176b)
[makefile] remove build.sh (8c9cf59)
[makefile] remove generate.sh (f0b3169)
[makefile] terminate if git checkout fails (ee637cb)
[makefile] uninstall feeds (126190a)
[makefile] use absolute paths (bfc499d)
[makefile] use git branches. Disable AA, enable BB by default (671ee3e)
```

