# Changelog

## Version 1.0.0

Firmware:
```
20e25c82d6 Makefile: do not include git-revision in filename of releases
708240926d Makefile: prefix images with "hedy"
caa7958715 packages: remove "migration" for Hedy-1.0.0
23de946c74 config: explicitly add options regarding version-info in filenames
ec06e30ea4 Makefile: add setting "SET_BUILDBOT"
cad82aea78 Makefile: add BUILD env "IS_BUILDBOT"
64cd8de4b1 patches: do not run policy-routing script on interface ffuplink
c81f697d9a Revert "profiles: disable all 4MB-targets"
ba3cb3f41e netifd: update to git HEAD version (2017-03-07)
5550d6bb52 configs: add package ffuplink-notunnel
da52348b99 packages: change "default" as notunnel-setup
0b7aa08806 Add "diffutils" and "patch" to optional packages
d3c50b6d67 hostapd: disable 802.11 legacy-rates by default
696871104f Add Raspberry Pi 3 configuration
7251b6648f added RaspberryPi configuration
398aee0684 configs: in preinit and failsafe change network to 192.168.42.1/24
1b45bfce15 patches: use olsrd v0.9.0.3
a0d1ca0ecd backport Ubiquiti ERX SFP to LEDE 17.01
590a07ef19 profiles: remove GL.iNet GL-MT750
972e689370 assemble_firmware: skip usecases with empty package-list
3dd9eaf575 Allow ICMP for busybox traceroute
8f5085c6f6 configs: build kmod-nf-nathelper-extra as module
789cb17c6a packages: add libustream-mbedtls to default and backbone package set
cdfd3b0b5e add packages to support ipip-tunnels
0ce68fcba0 profiles: add ubnt-erx-sfp for ramips-mt7621
4176688fc3 patches: add Ubiquiti EdgeRouter X-SFP (UBNT-ERX-SFP) support
35e8419d27 packages: add tcpdump to the default package set
f8dc9aa640 profiles: add TP-Link WR1043ND-v4
8765a27ee5 added some buffalo ar71xx targets
97eef0a600 Makefile: new target images to only create the firmware-images
fa11c670b6 profiles: enable TPLink Archer C5 V1
ac6dd7c412 configs: add iperf3 and collectd-modules conntrack, irq
d02b09ff62 configs: add PPPoE-support
6621d89260 README: add TARGET ramips-mt7621
9a331fb011 configs: remove deprecated 6to4-package
86330521ff Makefile: IB_BUILD_DIR is obsoleted by assemble_firmware.sh
cdc1404263 Makefile: remove unused TOOLCHAIN_PATH
86e155c2df configs: select collectd-dhcp-addon by default
e7b8a364d5 Makefile: define separate target for VERSION.txt
38d96a486e assemble_firmware: check for usecase-file
105d293ef9 assemble_firmware: check for files in embedded-directory
ef11714b86 Makefile: fix embedded-files/
274cd8131a add arch ramips-mt7621 to build for EdgeRouter X
d1d7755eaf profiles: add GL-Inet GL-MT300A, GL-MT300N, GL-MT750
827d03c43e profiles: disable all 4MB-targets
785c9bde58 configs, packages: use OpenVPN-openssl for RSA1024-keys
b8292dec06 configs, packages: uhttpd-mod-tls has been removed
f9de53e543 configs/common: use px5g-polarssl instead of deprecated px5g
d65f5fa17b configs: enable telnet client
d2f4aa74bb configs: disable "HORST", which fails to build
ebe7cf9bff assemble-firmware: add parameter "-e"
a66896d3ca Makefile: use openwrt/files to embedd files directly into image
```

packages:
```
2e44ee693 network-defaults: setup the ip rules at runtime
2df127c7a network-defaults: prohibit traffic to net on ffuplink
08474427d uplink-notunnel: setup default-route via hotplug.d
5e8f501c2 wizard, uplink-files: add uci-setting to request different auth-types
19cb3cddd dhcp-defaults: don't announce as default-gw
98f0a3442 ffwizard: adapt to new hostname from "system-defaults" package
a29d9a4d3 system-defaults: change the default hostname
a940a00df rename interface "ffvpn" to "ffuplink"
b9d449fb1 network-defaults: set "wan" as bridge
07483a62b migration: fix "set VPN03-connection to UDPv4 only"
e284bc9bd add new package: freifunk-berlin-uplink-tunnelberlin-files
02fb2519b firewall-defaults, wizard: add separate zone ffvpn
1288c3dc9 ffwizard, migration: don't create cronjob to restart "wan"
a08be1521 freifunk-defaults: change our settings, which differ from upstream
e7e850669 firewall-defaults: only commit firewall settings in UCI
7aff3d7fd freifunk-defaults: don't copy non-existing files in Makefile
c3af984c9 Merge pull request #113 from freifunk-berlin/freifunk-defaults
b0ae29f3c Merge pull request #107 from freifunk-berlin/ffwizard_remove-privateAP
1a52c4caa Merge pull request #112 from freifunk-berlin/olsrd-ipversion-6
e75872789 Merge pull request #115 from freifunk-berlin/add-system-status-page
5a0bc08c9 Merge pull request #114 from freifunk-berlin/bugfix-olsr-status
74c3d3fa5 Merge pull request #116 from freifunk-berlin/policy-routing
bdf56f482 Merge branch 'owm_cleanup'
d4521b1b4 luci-app-owm: bump version
fa8619e2a freifunk-berlin-freifunk-defaults: use uci-default script
e6e396507 freifunk-berlin-olsrd-defaults: explicitly set IpVersion to 6 for olsrd6
41ea9464b guard: add function "rename_guard <src> <dest>"
8b7e40011 openvpn-files: depend on virtual-package openvpn-crypto
d8a9c5eb2 lua-app-owm: adapt code to new wifinets and wifidevs api
b8540100d luci-app-owm: remove neightbl specific code
f845b3bb3 ffwizard: drop private AP-feature
6fe8f081f ffwizard: switch to new path of upload-dir
```
OpenWRT
```
d5278cc48b kernel: bump 4.4 to 4.4.112 for 17.01
2603c85060 wireguard: bump to 20171221
7f78a86254 hostapd: set mcast_rate in mesh mode
91e48304a9 openvpn: add support to start/stop single instances
77e79b2dd0 openvpn: update to 2.4.4
c7234e3036 imagebuilder: add package_list function
108a42bcba ramips: support jumbo frame on mt7621 up to 2k
f0a493160c mac80211: gracefully handle preexisting VIF
f173464f13 base-files: add generic board_name function to functions.sh
b41a2e646e opkg: bump to version 2017-12-08
f5f5f583f9 hostapd: backport fix for wnm_sleep_mode=0
3590316121 dnsmasq: backport infinite dns retries fix
e626942c33 dnsmasq: load instance-specific conf-file if exists
17.01-4
d501786ff2 hostapd: add wpa_disable_eapol_key_retries option
b6c3931ad6 hostapd: backport extra changes related to KRACK
a5e1f7f5ef mac80211: backport kernel fix for CVE-2017-13080
46e29bd078 x86: partly revert cabf775
707305a19d mac80211: Update wireless-regdb to master-2017-03-07
907d8703f4 wireguard: add wireguard to base packages
bff16304b0 brcmfmac: backport length check in brcmf_cfg80211_escan_handler()
fa0b5fce1f kernel: bump 4.4 to 4.4.92
e6fd17d04c ramips: fix compile warning in MT7621 NAND driver
2e9f3c6225 ramips: fix typo in MT7621 NAND driver
63c17142c8 hostapd: merge fixes for WPA packet number reuse with replayed messages and key reinstallation
cdd093b539 x86/64: add xen DomU support
cabf775e64 x86: Refresh subtargets kernel config
da0219ed9f x86: Fix xen serial console by removing conflicting PATA driver
f52b404aee x86/generic: use HIGHMEM64G instead of HIGHMEM4G to fix PAE and Xen
8ad1b09c6d kernel: add fix for bgmac with B50212E B1 PHY
c1023c8075 mt76: sync with version 878456caf60d from master
baa8eaaba6 bcm53xx: backport DTS changes up to the first 4.15 queued commits
94aa2b8af0 ar71xx: add rssileds to WA850RE v1 image
f67c22e0c2 toolchain/gdb: update to version 8.0.1
067221360e cmake: fix build error with Xcode 9 on macOS 12
a999f91ca3 gcc: fix build error with macOS + Xcode 9
2ce9c84a92 build: add a darwin sitefile to deal with macOS 10.12 + Xcode 9 build errors
f9a849ca84 ramips: mt7620: do not pad sysupgrade Archer images
ee32de4426 LEDE v17.01.3: revert to branch defaults
df54a8f583 LEDE v17.01.3: adjust config defaults
d0bf257c46 uhttp: update to latest version
783465d783 odhcpd: don't enable server mode on non-static lan port
c92c1894a5 odhcpd: backport fixes from master branch (FS#402, FS#524)
4b4a4af814 dnsmasq: bump to v2.78
b8357e87d7 base-files: create /etc/config/ directory
3350137bd3 sunxi: clean up modules definitions
a881323cb2 ltq-vdsl-mei: revert disable optimized firmware download
f483a35f08 curl: fix security problems
e232c6754d mbedtls: update to 2.6.0 CVE-2017-14032
37e1bd27d0 generic: drop 704-phy-no-genphy-soft-reset.patch
720b0e2e2d kernel: update 4.4 to 4.4.89
b428f45c06 ltq-vdsl-mei: disable optimized firmware download
39e5cd9556 ltq-vdsl: fix PM thread suspend and resume handling
86f0e8b091 openvpn: add "extra-certs" option
af802bc687 lantiq: fix missing otg_cap on danube platform
12a0da6315 tcpdump: noop commit to refer CVEs fixed in 4.9.2
f66c6e1d8a tcpdump: bump to 4.9.2
a131f7cb69 utils/tcpdump: Rework URLs
7f1359c14e base-files: fix wan6 interface config generation for pppoe
97ebdf93a3 ipq806x: Archer C2600: fix switch ports numbering
d33f7905df treewide: fix shellscript syntax errors/typos
4f162ac3ce ramips: fix hg255d LED status support
415175246e ar71xx: fix MAC addresses on TP-Link TL-WR1043ND v4
082e6215b7 hostapd: fix iapp_interface option
ab305e147e kernel: update 4.4 to 4.4.87
1d15a03050 dnsmasq: backport arcount edns0 fix
a7506c0e2b dnsmasq: backport official fix for CVE-2017-13704
bb6a8b2cbf uclient: update to 2017-09-06
ca53effdd6 kernel: update 4.4 to 4.4.86
1100bbf833 brcm47xx: refresh Linux 4.4 config
f62a31d0e9 f2fs-tools: fix mkfs.f2fs on big-endian systems
c3bddb49ff f2fs-tools: drop musl compat patch
707a4b459d f2fs-tools: drop patch in favour of CONFIGURE_VARS
bd29aa1ba1 f2fs-tools: Switch to gz tarball
a006b48c04 dnsmasq: forward.c: fix CVE-2017-13704
dc8392f6a1 kernel: backport usbport LED trigger driver support for DT
86722ab0bb kernel: fix of_node handling in LEDs core code
4a1b87aba4 kernel: update 4.4 to 4.4.83
cae20f64b5 bcm53xx: backport DTS commits that setup USB LEDs
ae3c55666d tcpdump: Update to 4.9.1
3e35eb13ad mbedtls: Re-allow SHA1-signed certificates
ff414fb575 ramips: fix WHR-1166D WAN port
889638c8bf base-files: don't setup network in preinit if failsafe is disabled
b67b316dd1 dnsmasq: backport remove ping check of configured dhcp address
4503d8b297 procd: update to the latest git HEAD
982612dba2 ramips: ArcherC50v1: fix wlan2g MAC address
48798af6d2 ramips: fix Omnima MiniEMBWiFi image
1a050c83ac ramips: build HuaWei HG255D image
57a8f36ac4 ramips: add missing partitions
66b071fa09 procd: update to latest git HEAD
6f4a903533 ralink: fix rcu_sched stalls on mt7621
c407e6c2f2 ramips: Archer C50v1: fix power led
8e67c358e7 ramips: Archer C50v1: fix switch port numbering
a9439344e7 ramips: Archer C50v1: fix LEDs active levels
5e409f0e69 ramips: fix Mercury MAC1200R v2.0 board name
5e87b01275 brcm63xx: add NULL clock fix send upstream
2247af82df ramips: add NULL clock fix send upstream
1807a0ef83 ar7: add NULL clock fix send upstream
7ab8bf126e curl: fix CVE-2017-7407 and CVE-2017-7468
69acb2533a kernel: update kernel 4.4 to version 4.4.79
a5822dbd0f ramips: DIR-860L-B1 fix switch port numbering
823d35f2fd kernel: netfilter: fix nf-nathelper(-extra) description
e08b8255ec ramips: fix wps button gpio for DWR-512
ece85e2e49 ramips: DTS: VoCore2 improvements/fixes
870ca0da7a ar71xx: fix switch port mapping for TP-Link TL-WR74xN/D series
671fc88c91 uboot-envtools: add support for ALFA Network AP121F
3959110c5b ar71xx: add support for ALFA Network AP121F
f6907dcc79 image: fix ar71xx legacy images
8fbef4b11b imx6: fix DualLite/Solo GW551X board detection
82b20d74cb procd: backport kernel watchdog start/stop support
c047c344c6 x86: add missing kernel config symbols to Geode target
05643bd64d x86: enable ACPI support for the Geode subtarget
699e3127c5 dnsmasq: backport patch fixing DNS failover (FS#841)
d0ec502510 ar71xx: set US region code for TP-Link TL-WR710N v1 image
7896d7b814 fstools: backport fixes from master branch
74d5c3e019 mtd-utils: use source package name for lzo in PKG_BUILD_DEPENDS
3214e174a0 ramips: fix Xiaomi MiWiFi Nano firmware partition size
27da508749 build: fix kmod package build on non-GNU systems
d71ffb9639 ar71xx: Fix UBIFS work on Mikrotik RB95x devices
52617669c2 lantiq: use img file extension for DGN3500 factory images
91d41b6305 dnsmasq: backport tweak ICMP ping logic for DHCPv4
cca765f64c dhcpv6: add missing dollar sign in dhcpv6 script (FS#874)
eff3469510 procd: backport fixes from master branch
8d3d7f6b52 kernel: update kernel 4.4 to 4.4.74
53eba6f58f ipq806x: fixup thermal patches
761e6087ed base-files: fix PKG_CONFIG_DEPENDS to include version.mk entries
f197a2a4c9 bcm53xx: include wpad-mini only on devices with (supported) wireless
6c03b293bb firmware-utils: fix dgn3500sum compiler warnings
73a4568f19 ca-certificates: Update to version 20161130+nmu1
57289ae640 openvpn: update to 2.4.3
73e81a8318 mbedtls: update to 2.5.1
5b0b27eb48 bcm53xx: enable Northstar thermal driver
c03d4317a6 kernel: backport Broadcom thermal drivers
8f254e9c27 Revert "dnsmasq: don't point --resolv-file to default location unconditionally"
c16326cfed dropbear: fix service trigger syntax error
2e206c79cc ramips: fix Phicomm K1S(PSG1208) pinmux
a6b5ddfd9b LEDE v17.01.2: revert to branch defaults
2da512ecf4 LEDE v17.01.2: adjust config defaults
65eec8bd5f build: ensure that flock is available for make download
4053c4f0fe include/toplevel: set env GIT_ASKPASS=/bin/true
e5db08edf7 base-files: network.sh: fix a number of IPv6 logic flaws
8a42d4d851 mwlwifi: update to version 10.3.4.0 / 2017-06-06
f709597e81 automake: import upstream fix for perl 5.26
df4363b607 base-files: network.sh: properly report local IPv6 addresses
4fbd072624 kernel: update kernel 4.4 to 4.4.71
443d705e38 Add missing APU1 reference to x86 board.d
524ed5088e base-files: always set proto passed to _ucidef_set_interface()
bf6216e5e3 lantiq: fix broadcasts and vlans in two iface mode
36ccbbdab1 lantiq: select kmod-mt7603 instead of kmod-mt76 for WBMR-300HPD
4186d737f6 lantiq: use the P2812HNUF* wan port as wan
254bf7961e lantiq: xrx200: use vlan for ethernet wan port
b78bcdf619 x86: disable X2APIC support for legacy subtargets
e78a641f52 umdns: remove superfluous include in init script
cdfc6788a9 dnsmasq: bump to 2.77
9e20cc56b9 dnsmasq: make tftp root if not existing
ebf46d2c5b dnsmasq: use logical interface name for dhcp relay config
78edfff530 dnsmasq: don't point --resolv-file to default location unconditionally
b1257d8d73 ar71xx: fix Wallys DR344 GPIO-connected LEDs and button
21a7e40941 ar71xx: set GE interface as wan by default in Wallys DR344
a412350684 ar71xx: fix GE interface support in Wallys DR344
dfecce60e6 toolchain/gdb: update to version 7.12.1
fe5e343933 usbmode: update usb-modeswitch-data to 20170205
4baf0ea229 usbmode: update to latest version
7c1e58863c usbmode: Update to latest HEAD
22478bf473 samba: bump PKG_RELEASE
757353c3a0 firewall: resync with master
4bd3b8f8b0 mac80211, hostapd: always explicitly set beacon interval
e194e1b3c8 hostapd: add legacy_rates option to disable 802.11b data rates.
20198f7330 ipq806x: fix Netgear X4 R7500 ath10k firmware selection
784ceba269 treewide: select ath10k firmware explicit
0e31ce730f ath10k-firmware: do not select the qca988x by default
a44d7bfb63 build: fix possible issue with kmod package having multiple AutoLoad's
e02b12c4cf kernel: update kernel 4.4 to 4.4.70
2f92622ce8 kernel: fix autoloading arch-specific modules
9c2bd3d631 backlight-pwm: fix module description
215c1d05b8 kernel: update kernel 4.4 to 4.4.69
d1a0fc3ec8 binutils: fix build with host gcc < 4.9
d179aa8769 util-linux: fix build with uclibc
dd19a41520 dropbear: bump to 2017.75
51db1f5a9a samba: fix CVE-2017-7494
1165c0ae0d umdns: update to the version 2017-05-22
74100f3788 bcm53xx: add support for TP-LINK Archer C5 V2
dfe2cea9cd firmware-utils: tplink-safeloader: add support for Archer C5 V2
0bef8f8011 fstools: backport regression fix for volume_identify
379155dc0f imagebuilder: fix bundling of DTS sources
dbaaeae428 image.mk: Generate cpiogz with root-owned files
4bd98e9224 ramips: add om-watchdog to rut5xx DEVICE_PACKAGES
9423cf3e98 om-watchdog: add support for Teltonika RUT5xx (ramips)
38367c5699 om-watchdog: cosmetic code style fixes
da4992f822 om-watchdog: cleanup Makefile
8011215ad2 ar71xx: enable nand-utils in the mikrotik subtarget to ensure it makes it to initramfs
aba1b3cbd1 openvpn: update to v2.4.2
53e751e303 openvpn: add myself as maintainer
d40e2efa94 OpenVPN: Update to 2.4.1
98491a9ae9 openvpn: add extra respawn parameters
bc58099802 openvpn: move list of params and bools to a separate file
7f3ec01069 ramips: fixup-mac-address: add missing include
d8cfebaa50 dnsmasq: support dhcp_option config as a list
d1e0cc8cd5 bcm53xx: backport DT patches for serial, thermal and MDIO
8619683037 ramips: add factory firmware for Tp-Link C20i/C50
d90ff22c8c brcm63xx: fix invalid Asmax AR 1004g DTS reference
d49920e450 lantiq: fix avm fritz box mac addresses
79cd14152c ramips: enable ramdisk for mt7621
bc0de2751c ipq806x: fix EA8500 switch configuration
0c8f72639f base-files: implement ucidef_set_hostname(), ucidef_set_ntpserver()
eb11207397 mac80211: rt2800: fix mt7620 E2 channel registers
64fa4ead32 mac80211: rt2800: fix mt7620 vco calibration registers
820a39687d mac80211: rt2x00: fix MT7620 LNA gain and VCO-after-ALC
5b91d2b52e mac80211: rt2x00: import upstream changes and rebase our patches
ab7087e24f rt2x00: mt7620: make fixes requested upstream
4314646ac6 rt2x00: mt7620: yet another beauty session
ceefe616c8 mac80211: add rt2x00 debug symbols to PKG_CONFIG_DEPENDS
5ac51ada60 ath9k: fix power limits on init
a9728799bc ath: do not apply broken power limits with ATH_USER_REGD
503e496366 odhcpd: update to version 2017-04-28 (FS#595)
c266641acf odhcpd: update to version 2017-04-21
37cf921352 build: fix symlinked .config handling
8b9f7bd7bd ramips: WN3000RPv3: do not setup switch
bf534e45ea brcm63xx: Add Observa VH4032N support
105d5b6f03 cns3xxx: use proper macro's for ID handling
49ce6d04b0 ramips: add support for Sanlinking D240
58ec566331 ar71xx: select ATH79_NVRAM only by boards actually use it
7e2ad9cbb8 ramips: fix Sercomm NA930 compatible string
88cc06abb7 ramips: remove Planex CS-QR10 sound device tree node
f1f0b92a79 ramips: cleanup SPI flash device tree properties usage
6aa0a85fc6 ramips: remove DT pcie nodes for GL-MT300A/N
e200c66a1a rpcd: Explicitly link with lcrypt
28d626556d ramips: ZyXEL Keenetic Omni/Omni2: export gpio usb power
fd693bc0e8 ramips: ZyXEL Keenetic Viva: align factory images
5b2624d618 ramips: ZyXEL Keenetic Viva: export gpio usb power
a66623639a ramips: add ip17xx support to WLI-TX4-AG300N
0405851eb2 ramips: fix EX2700 wireless mac
a12655a840 ramips: ZyXEL Keenetic series update wan mac
94948252e2 ramips: ZyXEL Keenetic Omni align factory images
85bca2d0fb ramips: correct keenetic-series switch index
1aee42c6a9 ramips: add support for Netgear WN3000RPv3
846457fdbf ramips: fix mac address of miwifi-mini
7ee09377e7 feeds: add option to force feed update despite modified files
0f3c2d031a ramips: Clean duplicated status property for Omega2 WMAC in dtsi
26f07f668a ramips: fixed sms led polarity into dwr-512 DT
dbd2212205 ramips: WN3000RPv3: do not setup switch
ae0e167f2b busybox: revert accidential version bump
fe0b171372 busybox: nslookup_lede: mimic output format of old Busybox applet
a2ee9b7068 busybox: nslookup_lede: fix compatibility with v1.25
af1d1ebdda x86: enable 4G high memory support for generic (32bit) subtarget
3bfe7ee632 generic: keep module aliases inside .modinfo
2bc8d5eaf1 ubox: bump to version 2017-03-10
1ab41265c3 kernel: use skb_cow_head() to deal with cloned skbs
1d1935b242 ar71xx: fix minor syntax error in /lib/upgrade/platform.sh
9117ef8d6a ramips: update DEVICE_PACKAGES for Ubiquiti EdgeRouter X
72fcdb6286 openssl: Use mkhash for STAMP_CONFIGURED
5feb4f0e6d busybox: fix build of nslookup_lede applet without IPv6 (#728)
449880e0ff busybox: Move libresolv detection to LEDE Makefile
9437fbb7ab bcm53xx: backport BCM5301X patches
3ff31f8a78 bcm53xx: parepare for building more Linksys images
ad145e03cc bcm53xx: prepare for building Archer C5 V2 image
3dbc4175a8 ar71xx: add TP-LINK TL-WR841N/ND v12 image
7eb58cf109 utils/f2fs-tools: Update to 1.8.0
1d76542cca busybox: add musl compatible nslookup replacement
6ca5ccc620 kernel: update kernel 4.4 to 4.4.61
c2999ef592 odhcpd: update to version 2017-03-29 (FS#635)
a532aaa2aa odhcpd: update to version 2017-02-28
425c6d0462 odhcpd: update to version 2017-02-21
f2f672c32c ramips: add RP-N53 pcie wireless eeprom
f3dc2ffdd4 ramips: fix WHR-600D eeprom dt property
caaa214eae util-linux: re-enable parallel builds
0faf921a01 util-linux: unconditionally enable ncursesw support
f2a3653882 utils/util-linux: Update to 2.29.2
c6e79980b8 build: fix triggering opkg/host compilation
5866ff8be8 libubox: fix host build on macOS
293c54c567 libubox: add host build
5aa97e35de opkg: switch to LEDE fork (#120, #551, #571)
7099bb19b5 mt76: ensure that the metapackage gets built as .ipk
53fcaed1f7 image.mk: force kernel rebuild on every run
638ca50f3b kernel: Fix the incorrect i_nlink count after jffs2's RENAME_EXCHANGE operations.
47bf110cbb mac80211: backport an upstream fix for queue start/stop handling
a49503bbc7 sysntpd: restore support for peer-less (standalone) mode
1bdd23231b ar71xx: fix Wallys DR344 ethernet MAC addresses offsets
0cb669b469 ugps: fix and improve init script
0dcc4d239d kernel: update kernel 4.4 to 4.4.59
1adc6db036 ubox: fix sha256 mirror hash
298c40fd34 odhcpd: fix sha256 sum
910a9430a0 firewall: document rules for IPSec ESP/ISAKMP with 'name' option
1b94737824 iw: enable MESH ID in scan output
0d304d4228 busybox: vi: backporting patches to fix ZZ and :x command
474c31a20d umdns: update to the version 2017-03-21
ba076ebbc5 umdns: update to the version 2017-03-14
0f23e80c27 iproute2: fix ip monitor can't work when NET_NS is not enabled
111cf1b9f3 curl: fix CVE-2017-2629 SSL_VERIFYSTATUS ignored
c4ed92ae7d mbedtls: update to version 2.4.2
7d70ad66ac mac80211: mwifiex-sdio: select DRIVER_11AC_SUPPORT
7ae68124a4 mac80211: mwifiex-pcie: select DRIVER_11AC_SUPPORT
fc90e87b65 mvebu: wrt3200acm enable SDIO interface
c03083339a mac80211: add support for Marvell 802.11n/802.11ac SDIO Wireless cards
9d84accea1 brcm2708: remove duplicated gzip from image generation
1bba5789af ar71xx: add ath10k driver and firmware for Netgear R6100 to firmware image
0eed4a61b9 umdns: update to the 2017-03-10 version
4a405ac8f9 brcm2708: add support for the new Raspberry Pi Zero W
e091e8951d brcm2708: order boards and models alphabetically
8b52a8906b brcm2708: update linux 4.4 patches to latest version
b3ba3764d0 brcm2708-gpu-fw: update to latest version
f8e08ffd94 ramips: fix Linksys RE6500 switch port mapping
20a2db83de ppp: propagate master peerdns setting to dynamic slave interface
09a8183ce8 kernel: update kernel 4.4 to 4.4.52
514854d636 bcm53xx: backport accepted BCM5301X and BCM53573 patches
0c05cadeb7 bcm53xx: include Broadcom PHY driver in the kernel
f4fc12f023 kirkwood: fix include in etc/board.d/02_network
21903d056e wireless-tools: Change download url to github
f0e8470aa9 grub2: update to 2.02~rc1
1b2a54b5cd iftop: bump to latest upstream
3d52251df4 swconfig: Bugfix switch_port uci option parsing
df041b6520 netifd: fix stopping netifd + interfaces
87e021e6e3 libpcap: add optional netfilter support
2e67e8c90f archs38: only calculate entry point address when necessary
657e3ce8a2 arc770: only calculate entry point address when necessary
0f2757dce4 px5g: replace px5g-standalone with a statically linked variant of px5g-mbedtls
2e8545333a mbedtls: add --function-sections and --data-sections to CFLAGS
e3021e0308 scripts/feeds: Reuse TOPDIR if defined in environment
b036a22fcc kernel: add Chinese codepages
fffabd3c44 gen-dependencies.sh: fix handling variations in "file" output
2d5f8eb067 rstrip.sh: fix handling variations in "file" output
db7f80c587 libpcap: remove feature dependencies on kmod-* packages
00e4f6fd36 ebtables: update to last commit
8aa92deaf6 hostapd: mv netifd.sh hostapd.sh
2856c7e320 ath10k-firmware: update qca9984 firmware
3983b4ad0f ppp: honor ip6table for IPv6 PPP interfaces
352f92fe08 ppp: add pppoe-discovery to an independent package
31c2461e3f base-files: Added a deprecation notice on wifi detect
8bb839e85a base-files: Add wifi config to wifi command usage
cff47cacd1 ar71xx: fix platform_find_rootfspart()
e1e9d27655 uclibc++: patch bugfix erase() on derived __base_associative
e19fbd3297 ramips: fix Airlink AR725W device title
23fd4e65ba scripts: get_source_date_epoch.sh: fix mercurial support, add mtime fallback
37b0d547db ath10k-firmware: revert faulty PKG_SOURCE_DATE change from 7cb27b46
e591831430 ath10k-firmware: update qca9984 firmware and board data
8a3ac15a47 ath10k-ct: Support ath10k CT firmware for 9887 chipsets.
4bd0edc8fd scripts/getver.sh: append short git hash based on upstream commit
9451cd7c5b leds-apu2: Add PC Engines APU2 LED driver
65b05463d7 netfilter: re-enable TEE support for kernel 4.4
2b122a6750 gpio-nct5104d: Add nct5104d driver package
bc443b1052 x86/64: Enable GPIO sysfs & GPIO LED support
c5d8d8fd64 x86: drop ep80579-drivers
83d3e393bf 6in4: add missing colon when setting default ca_path
ee1cd31d2b procd: update to latest git HEAD
bc61c1328d procd: update to the latest version
709c326461 hostapd: fix feature indication
ef5cb964b1 relayd: fix making incomplete instance json data
77fb98ee41 relayd: remove old start-stop-service related code
b24273fe71 ppp: ppp6-up: add executable permission bit
5f5fae27b5 mac80211: hwsim: select DRIVER_11AC_SUPPORT and DRIVER_11W_SUPPORT
2b22e1d5c3 openvpn: adding key_direction to append_params.
6cb46adbc9 ubus: update to the latest version
fdc22b616c ubus: update to the latest version
4c9b45966e libubox: Update to latest version
67c2a176ce libubox: update to the latest version
bf53a8327f acx-mac80211: fix scan API error that could lead to a crash
f1336d2a70 iw: sync nl80211.h with mac80211 package
703515f889 mac80211: sync with master branch as of 9edff13abd97
d27dd6298b ath10k-ct: depend on kmod-hwmon-core, it gets used when CONFIG_THERMAL is set
0ce2d5b6bf ath10k-ct: fix kernel api compatibility issues
09620c0825 ath10k-ct: Fix performance of 2x2 hardware running 3x3 firmware.
0a3088cb4b mt76: split kmod package
39d03d9959 lantiq: fix broadcast packets leaking on the wrong vlan on xrx200
5fed9ef842 kernel: move upstream accepted bcm47xxpart TRX cleanups
5c1758d468 kernel: backport bcm47xxsflash support for reading 32 MiB flashes
349577adbf Revert "kernel: ar8327/ar8337: disable ARL access code to avoid lockups (FS#384)"
7fd494d4b2 ar8216: flush ARL table during reset after init_globals
f6d94b0dd6 cmake: skip build system check on compile
59508e309e dnsmasq: Add upstream patch fixing SERVFAIL issues with multiple servers
06f3b91902 kernel: update kernel 4.4 to version 4.4.50
5612114090 Revert "px5g-standalone: provide px5g via PROVIDES"
4d1ab84f1e uboot-kirkwood: fix goflexhome/net bootcommand
cdeb2322ea ar71xx: Remove images for rb-941-2nd
f79926cb94 sdk: emit proper tag references for base URLs
0a26490fe4 lantiq: set the internet led interface according to wan interface
6a6e3a4928 lantiq: introduce lantiq_is_vdsl_system
c5879b0676 lantiq: fix ARV7519RW22 switch port indexing
c835c9ebe5 uhttpd: use sha256 when generating certificates with openssl (FS#512)
6ebb8723a6 dropbear: bump PKG_RELEASE
f527436364 dropbear: enable SHA256 HMACs
f88bd7cd0f ar71xx: fix ethernet PLL configuration for QCA956x
828a024c81 x86: Set default baud rate on Geode images to 115200
63a8424702 x86: Add Geos profile for Geode subtarget
808f6a500c x86: Add board configs for the PC Engines APU2
6d6db65d82 x86: Enable DIAG LED on Geos
bd5b5c749a x86: Move Traverse Geos configs into x86 base-files
06e0c30336 x86: Add configuration back for Traverse Geos
982dd01ac3 Mark targets using kernel 3.18 as source-only
25b7295617 ramips: fix the number of uarts for MT7688
71ea3b4814 ramips: fix PWM pin mux conflict in dtsi
44aec27112 ugps: fix typo
7efe538ac1 brcm47xx: fix button inversion for Asus WL-500W
be007c580e brcm47xx: fix USB driver choice for Asus WL-500W
dbb8e04472 qos-scripts: fix module load commands (FS#438)
853bad5af2 kernel: fix crashes on MIPS when loading kernel modules under memory pressure
df49e49bc7 mdns: update and rename package to the umdns
72d045b2a6 ar71xx: fix DEFAULT_PACKAGES for mikrotik devices
b8c9ded999 build: add buildbot specific config option for setting defaults
eea6df8255 tools: patch-image: fix file descriptor leak.
30a4966053 octeon: only copy sysupgrade file if present
152f57f509 ar71xx: Add missing device package om-watchdog for MR1750
fcba5ee47a ar71xx: add OpenMesh A40 to OpenMesh A60 profile
f30f25c33e ar71xx: extract ath10k wifi board.bin for the OpenMesh A40 board
d6d9f256ff package/uboot-envtools: add OpenMesh A40 support
e6057ed207 package/om-watchdog: add OpenMesh A40 support
4a36180970 ar71xx: enable sysupgrade for the OpenMesh A40
552bc355d1 ar71xx: add user-space support for the OpenMesh A40
14add3f724 ar71xx: add kernel support for the OpenMesh A40 board
b194b3d97f ar71xx: create profile and build image for the OpenMesh A60 board
facbdec0b5 ar71xx: extract ath10k wifi board.bin for the OpenMesh A60 board
8785ebc471 package/uboot-envtools: add OpenMesh a60 support
eb383710e2 package/om-watchdog: add OpenMesh A60 support
b7361c5b35 ar71xx: enable sysupgrade for the OpenMesh A60
72c65c6213 scripts/om-fwupgradecfg-gen.sh: add support for the A60
5ad9164b9c ar71xx: add user-space support for the OpenMesh A60
72d8d8c6f3 ar71xx: add kernel support for the OpenMesh A60 board
a3061e57e8 package/uboot-envtools: add OpenMesh OM2Pv4/-HSv4 support
8a35c489ad package/om-watchdog: add OpenMesh OM2Pv4/-HSv4 support
d536c1d04f ar71xx: enable sysupgrade for the OpenMesh OM2Pv4/-HSv4
b2f3d9b05c ar71xx: add user-space support for the OpenMesh OM2Pv4/-HSv4
9f0f4c1494 ar71xx: add kernel support for the OpenMesh OM2Pv4/-HSv4
68ba0525a0 ar71xx: Remove the v2/v3 from the OpenMesh profile names
cbd69f7e4e procd: fix default timeout for reload trigger actions
367a3bb36f mvebu: append metadata to clearfog sd card images
4817e61f45 brcm63xx: Neufbox 6: fix switch by probing through DT
034a80009c sdk: clean scripts/config before packing tarball (FS#504)
e5060b32e5 ramips: added image size into dwr-512 DT
b72dcd5457 layerscape: fix adjust_link for 10G & 2.5G
57dfbac6ff ramips: Correct switch configuration for Newifi D1
32c9d467e3 lantiq: fix patching the wifi mac address on BTHOMEHUBV3A
e967f4dd27 ath9k: fix various issues in the airtime-fairness implementation
eac4851bfd kernel: MIPS: IRQ Stack: Fix erroneous jal to plat_irq_dispatch
02515f0187 brcm63xx: fix lzma loader for BCM6362
f49efcd325 brcm63xx: do a full reset phy cycle
921cecbdf8 brcm63xx: fix external interrupts on BCM6318
b8567cb44e odhcpd: update to git HEAD version (FS#396)
03ff2d7359 odhcpd: update to git HEAD version (FS#388)
f25d9cbe48 arc770: backport upstream fix for unaligned access
bd64568d27 procd: update to latest git HEAD
4e2c2b51f5 ramips: fix AR670W partition alignment
86bd886697 brcmfmac: improve Raspberry Pi 3 stability
083854f06f bcm53xx: add missing system.sh include
42f3c1fe1c arc770: fix broken upstream change
2ad4383b74 tcpdump: update to version 4.9.0
f2b885d82e bcm53xx: set Netgear R8000 USB LEDs
054ce1624c kernel: update kernel 4.4 to version 4.4.47
b786a5ffc3 kernel: bump to 4.4.46
c656cbc56b kernel: bump to 4.4.45
ee3067c588 Kernel: bump to 4.4.44
518bb7ae5a bcm53xx: refresh Linux 4.4 config
8ff8e51cda bcm53xx: image: use one style of adding TARGET_DEVICES entries
81f9cd56a2 bcm53xx: backport upstream DTS files for Linksys devices
29c0b575ee bcm53xx: use accepted BCM5301X patches for R8000 and Luxul devices
5c4b2eb3dd mac80211: brcmfmac: backport wowlan netdetect fixes
52add1988c mac80211: brcmfmac: backport PSM watchdog improvements
c578da6198 mac80211: brcmfmac: backport minor code cleanups
4b9bdb48d9 mac80211: brcmfmac: backport 4.10 fixes & typo fix
85d128f145 mac80211: brcmfmac: backport scheduled scan cleanup and chip support
e48b1c2c07 mac80211: brcmfmac: backport some old patches from 2016
e8f42223be mac80211: rename brcmfmac patches to use higher prefix
41dc50fc27 kernel: backport bgmac support for external PHYs
aec04e1deb kernel: use upstream accepted bgmac fix for BCM47186B0
f61044a9b0 kernel: rename bgmac patches to squeeze them
36288db2fd mac80211: start hostapd with logging wpa_printf messages to syslog
bc49d7902c hostapd: enable support for logging wpa_printf messages to syslog
a0bc62fe08 hostapd: backport support for sending debug messages to the syslog
3f9a194e04 ramips: fix Airlink AR725W factory image build
c53bb974b2 ipq806x: fix wireless macs
5ed23223fd bcm53xx: set WAN MAC address to don't share one with LAN interface
41de9a2e12 ipq806x: fixup nbg6817 internal mmc and switch configuration in DTS
1b51a49a9d ccache, samba36: fix samba.org addresses to use https
0224e32cd0 kernel: fix BCM54612E PHY support
bce140ebb9 musl: update musl to 1.1.16+ and switch to download from git
b313f0d189 ar71xx: fix netgear wndr3700 v1/v2, wndr3800/wndr3800ch switch port mapping
581285c6dc ar71xx: fix netgear wnr2000 v3 switch port mapping
0880105144 ar71xx: fix tl-wr841n-v7 switch port mapping
2a14335d95 mvebu: fix usb port leds
faea9bea44 mvebu: set fan_ctrl.sh only on mamba
e9b60b587b x86: add kernel module for sp5100_tco watchdog
af3ae4b37c x86: Add sp5100_tco AMD patches
d6a830ac7e octeon: fix mtd partitions for erlite on cmdline
9c915d1e7b ipq806x: Fix wireless support for Netgear Nighthawk X4S D7800
4d561b3a30 package-ipkg: Do not fail build without base-files
f8d8b60f1b Fix dependency for hostapd
4cd9625dd4 iproute2: cake: update cake support
4f5ff0041a kmod-sched-cake: Bump to latest version
d1d970e235 libtool: don't clobber host libtool infrastructure
e5bc7bff85 build: properly pass CPP and CXX flags in HOST_MAKE_VARS
83c9bfad1e build: introduce default HOST_MAKE_VARS for host-builds
82009d4e30 tools/cmake: remove HOST_CONFIGURE_CMD and re-distribute the args & vars
786160cd76 odhcp6c: use LEDE_GIT in package source url
4d9106afa6 odhcp6c: update to git HEAD version
02d511818f odhcpd: use LEDE_GIT in package source url
036cf93edf odhcpd: update to git HEAD version
cd99f3c744 odhcpd: update to git HEAD version
ef170bff32 odhcpd: update to git HEAD version
fe253bcb99 netifd: update to git HEAD version
718c201b82 base-files: add /etc/iproute2/rt_protos
754f474568 base-files: uppercase default hostname: LEDE
be7480cb5a procd: update procd.sh to disallow signal-numbers, enforce signal-names
7c5bc827b7 openvpn: ssl-enabled variants also provide a virtual openvpn-crypto package
acebb4a990 iproute2: cake: add 'mpu' minimum packet length support
06fca0c48b kmod-sched-cake: add 'mpu' minimum packet length support
ff813588fd hostapd: default to wps_independent 1
2f9568ac2a hostapd: expose wps_independent and ap_setup_locked as uci options
f9519636f5 mwlwifi: Fixes rewritten history hash and latest version
d7cae5f0b4 opkg: clarify messages and errors related to downloads
b2cd9b80ef ubus: update to the latest version
977eb2c019 ubus: update to the latest version
ea43d60c18 kernel: ar8327/ar8337: disable ARL access code to avoid lockups (FS#384)
d5b5339540 bcm53xx: fix LAN MAC address for devices that use eth2 originally
01888f90a0 ar71xx: add missing DEVICE_TITLE for mikrotik devices
198d73b26f ar71xx: Fix mikrotik subtarget default profile for device profile selection
0780fd5ee6 ar71xx: improve Mikrotik hAP Lite device support
2cf64afd4e ar71xx: mark soft_config mtd part as writeable for RB-941-2nD
51b6dd1aed ar71xx: fix up the kernel config for the mikrotik subtarget
3e4b00e6fa ar71xx: fix network config for Mikrotik RB411U
ca2a03d1f6 ar71xx: add support for RB-941-2nD
0656bee36b ar71xx: convert mikrotik routerboard support to UBI
e53e44a0ad ar71xx: create a proper default profile for the mikrotik subtarget, drop other profiles
47fa00a3d4 tools: update kernel2minor to 0.24 version
b2437a02a4 base-files: don't overwrite model name set by target
f4162bf3ca mt76: update to the latest version
e3849823e0 kernel: update bcma to fix devm memory leaks
5f2a1ac59a ath9k: remove the deaf rx path state check patch
406f85a328 mdns: update to the latest version
76f1b9457d download.pl: fix detecting download errors with curl
bda982b97f ramips: add missing DTS pcie node for WSR-600
e038c60049 qemu: rename internal crypto/aes symbols
4fa8f2a7a1 tools/qemu: use default host configure rule ; set appropriate vars & args
31b0640906 lantiq: fix unaligned access in xrx200_poll_rx()
ec095b5bf3 ledtrig-netdev: don't cancel work on events for different interfaces
b8fcbbf31d kmod-sched-core: Add HTB and TBF traffic shapers
70a6bbd53d ar71xx: prepare jffs2 partition properly in factory.bin for BHR-4GRV2
f5e8c908bd mxs: remove stale references to obsolete kernel module packages
69f773daa3 openvpn: add support for various new 2.4 configuration options
d46ce9498c kernel: backport support for BCM54210E PHY
c170848254 kernel: backport support for BCM54810 PHY
2ee7bc0a5e kernel: backport support for BCM54612E PHY
f5ab082243 openssl: update to version 1.0.2k
66211d0781 lantiq: fix brnImage signature for the VGV7510KW22BRN images
36db143690 ath9k: fix up a refcount imbalance error in the IRQ related fix
ecc362ed04 procd: update to latest git HEAD
a1f918cd92 base-files: fix user creation on sysupgrade with few opkg control files
04a5085127 include/rootfs.mk: keep Require-User lines with CONFIG_CLEAN_IPKG
dfe77be01f imagebuilder: properly escape single quotes in device titles
f9022964cf ath9k: add stability fixes for long standing hang issues (FS#13, #34, #373, #383)
acd1795a60 mac80211: refresh patch
a6f3ea5e84 Add back the commit "ath9k: Add airtime fairness scheduler"
6b68635047 bcm53xx: disable building Linksys EA6300 V1 image
e9ecb228c9 x86: fix sysupgrades on disks with 4k block size
e9d2173921 mac80211: brcmfmac: don't use uninitialize mem for country codes
81f2196bb1 mac80211: move (& update) upstream accepted brcmfmac patches
86b4b027cf brcm47xx: backport arch patch with Luxul devices support
806d3cc2c3 packages: mark packages depending on a target as nonshared
f6de4a5025 sdk: explicitely remove ccache directories when packing SDK
fc366fde07 lantiq: remove CPU_TYPE:=mips32r2, it gets overwritten anyway
b630d525c8 x86: unify CPU_TYPE for legacy and geode
c2ecf9c37a uml: mark as source-only
4d73b6b8d0 malta: mark as source-only to avoid wasting build resources
0a4d20fa9c malta: move FEATURES to the target makefile
392cccb7f4 build: remove mips16 feature flag from target makefiles
e775adead8 build: remove obsolete mips32r2 CPU_TYPE
6193e3cdee ramips/rt288x: switch CPU_TYPE to 24kc
b36e24f39e x86: remove the xen_domu subtarget
296772f939 x86/generic: add xen DomU support
b850218584 hostapd: fix stray "out of range" shell errors in hostapd.sh
ef08595c3f openvpn: let all openvpn variants provide a virtual openvpn package
3a9926e40f kmod-sched-cake: fix parameter passing kernel/user space
12392e5600 zlib: Update to 1.2.11
cfb3ef3a97 lede-keyring: bundle latest usign certificates
2c4d158d80 sdk: fix Git URL detection
cf5f7aa0b6 sdk: avoid using private repository clone urls as base repo entry
4039b3eba1 lantiq: fix an ethernet stability issue triggered by receving packets during boot
6538961d6a lantiq: fix spurious irq storm
c76da77573 git-kernel: $(SUBDIR) should always be $(LINUX_VERSION)
29a4a17f55 sdk: do not strip static libraries
c71e13a81a netifd: update to git HEAD version
2ac776ac76 curl: fix HTTPS network timeouts with OpenSSL
1e1e3ef2fb LEDE v17.01: set branch defaults
b9a408c2b4 base-files: add ARCH_PACKAGES to openwrt_release and os-release
5c20a4fec9 ubox: turn logd into a separate package
b5b83706be mbedtls: add static files in staging_dir
0b2991a8ed kernel: make ledtrig-netdev use a work queue for updates
9c55dede26 include/feeds.mk: base list of enabled feeds on available instead of installed feeds
621fd9fd62 opkg: use default PKG_BUILD_DIR
25200ae7a5 mac80211: brcmfmac: add early (& hacky) patch for storing country codes
5fba00a686 mac80211: use wiphy_read_of_freq_limits in brcmfmac
ea6d10d572 bcm53xx: add pending BCM5301X patches: Netgear R8000 WiFi & Luxul DTS
ee6cce6b31 kernel: fix bcma serial console regression
8004aa313a ipq806x: refactor ipq8065 device tree
ca25b4d729 ipq806x: enable hw pseudo random number generator
44b44595dc ipq806x: update eMMC and SDCC3 nodes in device tree
45bf3d4f24 ipq806x: disable usb3 phy suspend and add usb tcsr control
c067011af8 ramips: add back the i2c-mt7621 module
f4f2dd04bd mt76: select 802.11w support
ab90f15c89 ramips: Added Onion Omega2 and Omega2+
dea191914c kernel: can: Add missing regmap dependency for kernel 4.4
ace9d1fb6f ar71xx: Detect USB port on Mikrotik RB750UP
80768ddccd ramips: Add I2C driver to the default kernel config
26e4fee6e2 imx6: kernel: Backport serial port fixes
1708644f19 kernel: backport MIPS changes introducing a separate IRQ stack
b02636fcb4 gitignore: add /overlay
21baa25009 ath10k-firmware: Update QCA988X firmware to latest version
7e8fecb224 hostapd: fix passing jobserver to hostapd/supplicant build processes
40e4c342fd hostapd: backport a few upstream fixes
a206394efa mt76: update to the latest version, adds support for 802.11w
0d8381aea3 ncurses: revert $(STAGING_DIR_HOSTPKG) to $(STAGING_DIR)/host where appropriate
12d0a66942 include/autotools.mk: use STAGING_DIR_HOSTPKG where appropriate
e7e91e62bb mac80211: backport a fix for a tx related race condition
a46d1fde4b mac80211: refresh patches
adf2fef5e8 mac80211: backport some upstream fixes
5b089e45a6 kernel: update 4.4 kernel to 4.4.42
619c8fa922 imagebuilder: remove existing debug kernel image
d1514e8f84 imagebuilder: remove existing root filesystem images
c6a8a23ea2 xburst: remove hack to determine entry point
d2424d4b21 malta: remove hack to determine entry point
3e521fa112 sdk: exclude locale files to save some space
920170a27f firewall: fix forwarding local subnet traffic
9641ceea0c mvebu: simplify etc/board.d/02_network
f24ffb901e mvsw61xx: add support for MV88E6352
89ecfa7556 mvebu: several fixes for Linksys WRT3200ACM
8935689a8e mxs: gzip ext4 images
515d012e6d arc770: gzip rootfs image to save some space
113dd45092 archs38: gzip rootfs image to save some space
8af5e5751d image.mk: add generic function for gzipping images if enabled
6f57e32f95 mvebu: remove the clearfog-bundle
87b668765e image: when using the new image build code, gzip ext4 images by default
c914fa04a3 dnsmasq: use ubus signalling in ntp hotplug script
749918911d x86: disable crashlog
e38fd1eced x86: disable a workaround for a buggy glibc version
27fbf54147 octeon: disable ext4 images
402fea62c4 netifd: update to the latest version
859693509f image.mk: use LINUX_KARCH rather than ARCH for mkits
f44663c673 uqmi: mark as nonshared because of the usb dependencies
185b06f04a umbim: mark as nonshared because of the usb dependencies
1ca31b0931 comgt: mark as nonshared because of the usb dependencies
bd68ddbda4 polarssl: remove package
dcd8357365 armvirt: add kernel config change missing from 0d44f0cb
d6c77b9d99 ar71xx: default to external USB power on RB-912UAG
5919cc2dc4 build: let make check warn about use of legacy PKG_MD5SUM variable in feeds
6f9011f089 cmake: properly pass host cflags/ldflags to the build
7969770100 cmake: support verbose build that shows compiler commands
d6de31310c cmake: restore parallel build support for bootstrap
83eef37400 x86/64: enable the fusion scsi driver
2b6284f5a8 mac80211: fix broken spatial multiplexing defaults
544dee575d ath10k-fw: Update to latest CT firmware
5c09d7f23d ath10k-ct: Update to latest CT 4.7 ath10k driver.
0d44f0cbbc armvirt: enable the USB feature flag
627b0d3559 mountd: drop USB related dependencies
29097b95ba ramips: fix WLI-TX4-AG300N boot and network
3f31029b19 ramips: add support for VoCore2
d7fd1a0f8d ar71xx: enable serial console on Mikrotik RB411/RB433
287283e6e3 ramips: rt3883: fix typo in pinctrl lna_g_func
d1daf3f38d map: take over maintainership
0d49f9f4b4 odhcp6c: take over maintainership
5303d4bedb odhcpd: take over maintainership
ec63e3bf13 Revert "dnsmasq: change 'add_local_hostname' to use dnsmasq '--interface-name'"
bb8e9c51ab map: delete map-t device when tearing down map interface
1ad30be982 Revert the recent dependency and metadata scanning rework
fbe522d120 comgt: allow build without USB_SUPPORT
278ad007ee umbim: allow build without USB_SUPPORT
863888e44f uqmi: allow build without USB_SUPPORT
96daf6352f mountd: allow build without USB_SUPPORT
cfd83555fc scripts/package-metadata.pl: fix overriding conditional dependencies with conditional select
90f0ca0ddc arc770: build dtb files in Image/Prepare so that they are available for Device/*
b9713ad630 archs38: build dtb files in Image/Prepare so that they are available for Device/*
4ce3c41696 bcm53xx: backport upstream bcm53xx spi driver changes
2e1f6f1682 mvebu: work around an ethernet tx scheduling fairness issue
3be4c6ca93 kirkwood: only add UBI EOF markers for devices that need it
4d8da82c29 procd: add support for overriding the tar sysupgrade board name
e21cb649a2 ar71xx: disable sub-page writes on routerboard nand drivers
b7bee2858b kernel: remove linux 4.1 support
b1dbe6028e ar71xx: fix legacy image build error
1b17f4f260 arc770: fix parallel build issue
3fa2c77e3a archs38: fix parallel build issue
889272d92d ar71xx: fix RB4xx CPLD SPI device mode setup
c3a8b87773 ar71xx: fix RB4xx SPI driver mode bits
15f4fbb7bd mvebu: update mwlwifi driver to version 10.3.2.0-20170110
80dbaa4ef3 kernel: backport a MIPS SMP icache flush fix
7c8a36340c kernel: update bcm47xxpart failsafe partition patches
593240075f wpa_supplicant: Fix mesh encryption config
b95494baed gettext-full: avoid using iconv for host builds
43d5339940 tools: cmake: link librt if needed (FS#381)
69be65b594 tools: mkimage: pass crypto libraries through HOST_LOADLIBES (FS#381)
96a940308b tools: libressl: always build as PIC
77beaf2ec9 package: replace $(STAGING_DIR)/host with $(STAGING_DIR_HOSTPKG)
7480d3309c kernel: add missing config symbols
e9b49a41e2 kernel: add missing config symbol
f714fe46a9 mac80211: pending brcmfmac patches cleaning channels management
07df80a1a6 mac80211: rename b43 patches to make more space
90ed0aa859 build: scan.mk: consider KernelPackage pattern as well
1ce9b566fd procd: update mirror hash
c9dd40f628 kernel: remove gpiommc patches / driver
1a5cb4ac1b kernel: add pending bcm47xxpart support for failsafe TRX partition
ef9208c51e kernel: update spi-nor.h include fix with upstream accepted version
b4d2575add kernel: rename bcm47xxpart patches to fit more of them
a891e5e14f build: scan.mk: remove overlay broad grep pattern
01d9527357 kernel: remove DEVTMPFS platform overrides
c2fc52ae22 kernel: remove DEVMEM/DEVKMEM platform overrides
36167ae46c ath10k-firmware: update board data for qca9984
4ee4c24092 kernel: drop kmod-i2c-ibm-iic
96815fe0a2 kernel: remove omap24xx specific kernel module packages
7ff7be96dd omap: build various core drivers into the kernel instead of packaging them
10f7a8d648 kernel: add missing config symbol
f630342af2 kernel: simplify dependencies for kmod-via-velocity
5b92dca09f kernel: drop crypto-hw-ppc4xx
9cdf852ae0 opkg: drop S/MIME support
f5c649d7c6 mpc85xx: build i2c support into the kernel instead of packaging it separately
96ade7adae mpc85xx: build usb support into the kernel instead of packaging it separately
0b2b162db9 kernel: remove kmod-gianfar, it is already built into the kernel
c472ed29b4 kernel: remove kmod-ata-imx, it is already built into the kernel
cdcf7265fd lldpd: take over maintainership
046606a05e lldpd: add Net-SNMP AgentX support
0d3dc16931 ar71xx: drop references to madwifi
c687a70fdf iwinfo: drop references to madwifi
cc66f819b4 px5g-standalone: provide px5g via PROVIDES
06c76e41d7 ppc44x: mark as broken
43a528eb96 kernel: add missing config symbol
83b6bfc235 build: fix HOST_CONFIGURE_VARS placement
fe876e9ac6 mvebu: Fix up some leds on this series
72d751cba9 build: rework library bundling
38de638eae mtd-utils: mark as nonshared
acd0c8c178 kernel: move the gateworks system controller driver to an out-of-tree package
c00e5a4f09 mpc85xx: enable the crypto acceleration driver in the kernel config instead of packaging it
a2f6b56c8f imx6: enable the crypto acceleration driver in the kernel config instead of packaging it
93cbdde43a kernel: fix kmod-w1-master-mxc dependency
78de59f15a kernel: fix dwc2 gadget dependency
29443e2c94 mxs: remove modules.mk, select drivers in the kernel config
915d7db9bd mxs: remove obsolete kernel package depending on linux 3.18
64be6fe9ca mxs: enable the chipidea usb driver in the kernel config instead of packaging it
7450698957 imx6: enable the chipidea usb driver in the kernel config instead of packaging it
7f0796d874 imx6: remove kmod-thermal-imx, it is already enabled in the kernel config
348fedc1a6 imx6: build support for the ventana ethernet expansion board into the kernel instead of packaging it
c524d1b256 imx6: enable the Freescale SNVS RTC driver in the kernel config instead of packaging it
1e1d735e52 build: remove obsolete parallel build related options
029b36d9b5 procd: update to latest git HEAD
e3358b2cc1 malta: Fix README file examples
dfe93c20ec libnl: Update to 3.2.29
f2b6412c72 ramips: Fix VLAN limits for MT7621 GSW
1016a32919 usbutils: Update usb.ids database to 2016.10.13
6ebb46a40a ipq806x: fix pvs1_bin voltage in ipq8065 DT
e9f0b75976 cyassl: update to wolfssl version  3.10.0
f036956e1f lantiq: update USB controller initialization
2dac67464d lantiq: fix dma locking problems with SMP
828a471e8d tools: remove obsolete yaffs tool
a9232ba1ed tools: reorganize dependencies, fix build after deleting staging dir
589a16fdb6 px5g: remove obsolete reference to $(BUILD_VARIANT)
5903c46ef8 build: fix build of ubifs images
1c6b1ab01d imx6: fix image boot ubifs compression option
3e7b894ac0 ustream-ssl: remove legacy polarssl support
1cf64e210f px5g: remove legacy polarssl support
018d80007e kernel: remove ubifs xz decompression support
8d2171e469 odhcp6c: add option "keep_ra_dnslifetime"
f0353c5e8c mbedtls: re-enable CFB support
c1b12aa838 Makefile: ensure that BIN_DIR exists for diffconfig
d4ce3e8692 uboot-mvebu: enable loader with the default profile
355e150065 mbedtls: re-enable RC4 support (needed by transmission and others)
621f8cbfae odhcpd: bump to git HEAD
4061c8eb53 Revert "gdb: fix build with gcc 4.1.2 as host compiler"
186cd4533d zlib: update to 1.2.10
50a3bce3eb rb532: drop patch-cmdline from base-files
ad76fdfc8a rb532: switch to UBI, drop yaffs2 support, use sysupgrade for NAND
5b6b0aa267 rb532: convert to new loopback based overlay support
c2e6ca26e5 build: add image command for calling kernel2minor
b18f75c3d8 oxnas: minor kernel config improvements
69903c3ee6 oxnas: require image metadata
870b7bee44 oxnas: remove some kprintf calls from NAND driver
8f0dc92afd lantiq: fix console print for additional boards
88ca6390ea kernel: bump to 4.4.40
b9857b21c2 tools/kernel2minor: fix permissions of created files
188626f17c mac80211: backport cfg80211 support for ieee80211-freq-limit DT property
4235cd0d95 x86: add kernel module for AMD CS5535/CS5536 audio chipset
476e77c3b7 tools/kernel2minor: fix endian conversion issues, allow creating little-endian images
8782672b90 tools/kernel2minor: fix portability issue
7304510392 base-files: save /bin/mknod for sysupgrade
f277f45bd6 yaffs: fix to detect MLC/TLC NAND flash
d8dde8c517 lantiq: fix console print
b7e8de67e0 strace: update to version 4.15
612e2276b4 dnsmasq: change 'add_local_hostname' to use dnsmasq '--interface-name'
06e26363d8 dnsmasq: clean up white space in dnsmasq.init
1fef80f29c ar71xx: add support for TP-Link WBS210/510
2ee3e8dd42 firmware-utils: tplink-safeloader: add support for TP-Link WBS210/510 1.2
08d73bfdce tools: cmake: use different approach for passing LDFLAGS
267b05f273 Revert "build: fix HOST_CONFIGURE_VARS placement"
f9b253147a tools: cmake: use pkg-config to discover libcrypto linker flags
0c03650160 tools: mkimage: use pkg-config to discover libcrypto linker flags
bfb2512a4e tools: make libressl build depend on pkg-config
28f9df62f5 build: fix HOST_CONFIGURE_VARS placement
8160beb014 cmake: update to version 3.7.1
d2ddda691e build: ensure that prereq-build is run before metadata scan from feeds (FS#367)
fbe3e22507 uboot-sunxi: enable parallel build
0ac00c931c sunxi: use fwtool for checking sdcard images
5ece16fd23 sunxi: add sysupgrade support
8a2c56ca03 sunxi: make sdcard image with squashfs as rootfs
4eb0fd8283 sunxi: convert to new image generation method
6268d496a4 uboot-sunxi: add uboot-sunxi-all for selecting all other variants
6f61d8511e base-files: export x86 platform upgrade functions to common.sh
d53fcdefbf sunxi: enable loopback device and f2fs support
76ee28ce9d sunxi: fix dts name for Mele M9
4ebb13a0ef build: unzip: perform operations quietly
fa37bdc05a x86: move sysupgrade.tgz only if it exists
5f9e367127 kernel: spi: allow setting chipselect gpio to sleep
af79fdbe4a ar71xx: remove a non-upstream spi core patch
e3072599f6 ath9k: don't run periodic and nf calibration at the same time
84bd74057f build: use mkhash to replace various quirky md5sum/openssl calls
dad48c6438 build: add a small standalone utility for calculating md5/sha256 hash
a0993dda5f tools: make cmake depend on libressl, one of its utilities uses it
bdaa138c0d host-build: remove openssl include path from host cflags
f6e6341d89 tools: build libressl on all systems
a46c9a4038 oxnas: remove support for pre-4.4 kernels from drivers
ed69e93262 kernel/modules: add SSSE3 SHA512 module
86de53203e kernel/modules: add SSSE3 SHA256 module
159e82d0db kernel/modules: add SSSE3 SHA1 module
a93accd73d kernel: allow subtarget specific KernelPackage
301301da2b x86/64: enable AES-NI support in kernel
2406b3488f brcm47xx: generic: include Ethernet drivers in standard image
5f8e3386e0 brcm47xx: drop some personal profiles
d091b2c381 brcm47xx: generic: drop standalone profiles duplicating device ones
b138e690e5 brcm47xx: generic: specify DEVICE_PACKAGES for all devices
11c41a0ea9 brcm47xx: fix bgmac package
2a72a916ab build: add diffconfig target
38a8cea063 powerpc: boot: fix build with parallel make
18152e71d8 brcm47xx: mips74k: specify DEVICE_PACKAGES for all devices
1d74f78877 brcm47xx: legacy: specify DEVICE_PACKAGES for all devices
c296ba834d Revert "ath9k: Add airtime fairness scheduler"
10f91525bc dnsmasq: add DHCP Unique Identifier for DHCPv6
1175a5b153 odhcpd: bump to git HEAD version
34fa03ea16 odhcp6c: bump to git HEAD version
388681fe53 hostapd: enable SHA256-based algorithms
30f14f6198 hostapd: add function to handle wpa_key_mgmt
bdcffb9bb6 wpa_supplicant: rework wpa_key_mgmt handling
b13e103d71 ath5k: select 802.11w support
e2f866d63a generic: mtd: add lock/unlock support for f25l32pa
d6c831e0e5 generic: mtd: backport SPI_NOR_HAS_LOCK
799d0dddf6 layerscape: add ls2088ardb device support
1866368a8a layerscape: add ls1088ardb device support
c6d3a62919 gre: add different per-protocol prefixes to GRE-TAP IPv4/6 tunnel interfaces.
15d8d9c271 build: drop `trapret` function from non-Linux HOST_TAR variant
0bb474652e elfutils: bump to 0.168
fc6b6f4583 download.pl: use curl in preference to wget
558680012d curl: Remove PolarSSL and adjust default to mbedTLS
cd18ff9ed6 tools: gmp: Update to 6.1.2
0050b39fd4 gmp: Update to 6.1.2
6099f22097 zlib: Update to 1.2.9
bb4afdc8bc libusb: Update to 1.0.21
54ff3b1def xz: Update to 5.2.3
1618c4abdb rpcd: Update to 2016-12-03
9bf2bc7587 fstools: Update to 2016-12-04
55209a9df9 uclient: Update to 2016-12-09
91dab05918 ixp4xx: drop 3.18 config/patches
8c822ec4ca uboot-lantiq: fix boot of images larger than 8MB
cfe1c6debe uboot-lantiq: fix build with gcc6
b35a41c139 generic: backport dwc2 kernel panic fix
b28e94d4bf ramips: MiWiFi Nano fixes
fd718c5025 mac80211: Allow HT/VHT rates when running unencrypted mesh.
8496659eb4 base-files: fix message of initscript wrapper
5639e45614 generic: package Broadcom BNX2 driver
321aca6661 oxnas: fix syntax in ox820-akitio.dts
1436e15488 curl: update to version 7.52.1
3e2c60e476 oxnas: append metadata to sysupgrade image
5cde94d9ab oxnas: backport upstream NAND driver
ae21033e76 oxnas: drop support for kernel 4.1
1f7a3584e5 oxnas: switch to kernel 4.4
b7677f05d6 ustream-ssl: remove extra DEFAULT_VARIANT from libustream-polarssl
39d3a4117b openvpn: update to 2.4.0
8ed11ebf7d mbedtls: enable DHE-RSA key exchange
ca963bbf5f mbedtls: enable secp384r1 elliptic curve support
4731f02fa2 kirkwood: fix ubi partition name
83d59453c0 kirkwood: fix sysupgrade for non-dockstar NAND devices
8f5cf323c4 brcm47xx: drop standalone Netgear WGT634U profile
b1bdb6e5ea brcm47xx: specify DEVICE_PACKAGES for Netgear WGT634U
c5ca3043d1 bcm53xx: drop unused source file of bcm53xxspiflash
ef4fc00c91 brcm47xx: mips74k: fix typo in Netgear WN3000RP model name
939ef157da ramips: fix NixcoreX1 profiles
ae37f2310b mbedtls: enable support for external private RSA keys to fix openvpn build issue
19059d84a4 linux: correct deps for x86-xen-domu target
2fd5ce9488 libressl: disable shared libraries, fixes build issues
c9c68c7177 ath9k: fix issues with external reset on AR913x
6b524fe5b8 relayd: fix expiry time handling
3f20fd4ee0 relayd: fix reload / interface restart issues
9c402d03e6 kirkwood: enable initramfs images by default
f04b651453 ath5k: drop bogus warning on drv_set_key with unsupported cipher (FS#334)
00ad43f047 ath9k: remove old rx dma stop check optimization
1b5640be33 odhcpd: bump to git HEAD
e1d1c31890 opkg: vfork external gzip command to uncompress data
dc5f496a0d Revert "opkg: vfork external gzip command to uncompress data"
bdd2b67414 odhcpd: Use procd_send_signal in reload_service
d3489d899a opkg: add missing dependency on libpthread
94030e86d5 mwlwifi: Update to latest source
c24172cad1 package/Makefile & ipkg-make-index.sh: add full package data list
4c4047ec19 musl: refresh patches
2912f9f2a2 musl: backport various post-1.1.15 fixes
b97c933ffb musl: rename a custom backport patch
0090adcd5c opkg: vfork external gzip command to uncompress data
d109d03198 kernel: split kmod-lib-zlib into two packages to keep it in sync with kernel dependencies
2e41b2c37a netifd: Upstep to git HEAD version
4c9d2c04ba gre: Remove ttl default value assignment (FS#312)
4af4f21492 ltq-vmmc: mark VOICE_CPE_VMMC_PMC as broken
2e101b5e66 ppc44x: fix build of crypto4xx_core.c
9c49c937ab kmod-sched-cake: do not build on kernel 3.18
9998bc5ef7 lantiq: fix falcon build
f9226158be lantiq: rename EASY98000 to EASY98000NOR
6e7fdf07b7 kernel: add KERNEL_DEVMEM and KERNEL_DEVKMEM
236bf83bb6 brcmfmac: select 802.11ac support
41b63b50d1 rb532: remove linux 4.1 support
b69314ea99 rb532: Switch to kernel 4.4
002264d5b1 rb532: Backport fix to resolve oops during korina_restart
7a340a5cd0 rb532: Add support for kernel 4.4
db553ffb34 rb532: Fix initramfs kernel images
0a5ccfbadd toolchain/gcc: update 6.x to 6.3.0
16725e2db0 libpcap: Fix build when PACKAGECONFIG ipv6 is not enabled
ea9b71e5b1 lantiq: drop the FRITZ7360SL led-dsl alias
7dd42d610d lantiq: add FRITZ7360SL phy reset gpios
9aa420b00e lantiq: fix DGN1000B boot status leds
0cf581ca3a ramips: use new image build code for more devices
a75ce960ac ramips: use different board names for variants
29f5e643ad ramips: sort rt305x image file alphabetical
d2b1148e75 ramips: use D-Link DIR-600 B1 image for B2 version
d2b6bf1416 ramips: fix image validation errors
ae3ac76e56 ramips: use destinct 11AC NAS board name
a18488a0aa orion: remove linux 3.18 support
0d5ba94088 orion: enable SoC drivers in the kernel config
49e81f9fe4 kirkwood: clean up profiles, move to image makefile
9a1f441ac8 kirkwood: enable SoC drivers in the kernel config
44447f6882 kirkwood: clean up FEATURES
2eb1cc3dfc kirkwood: remove legacy image build code
c9e4cf2299 kirkwood: convert iconnect, ib62x0 and pogoplug_e02 to the new image build code
3f55e5aeb5 toolchain: remove ppl/cloog, disable graphite for gcc 4.8
8bf69ee78c kernel: Add kmod-ethoc
4f033b2da6 ramips: fix tplink image building fix sysupgrade firmware on MR200
3a6353d910 ramips: enablemodem: move /lib/ramips.sh to start()
29cc927ef5 generic: ar8216: fix invalid bounds check imported from ChromeOS (FS#347)
08db3e1b85 dnsmasq: add log facility option
43855793ca ncurses: rename libncursesw to libncurses (more common name)
d44c6ec1ce Revert "arm64: boot-wrapper: Add mirror"
18300db77a b43-tools: fix tarball hash
47cf238779 uhttpd: drop uhttpd-mod-tls, it has been useless for years
c7c1cf5618 treewide: clean up and unify PKG_VERSION for git based downloads
43c09f2885 Revert "linux-firmware: Add mirrors"
ffb0181a87 build: add defaults for PKG_SOURCE, PKG_SOURCE_SUBDIR, PKG_VERSION
24e58c3f72 mwlwifi: Update to latest source
0ee964f284 ath10k-firmware: update qca9984 firmware
acfb067835 gettext-full: enforce only static lib on the host build
1831e61699 x86/64: enable Hyper-V support in the x86_64 kernel config
528f46d082 ath9k: Add airtime fairness scheduler
600b824087 openvpn: use conditional dependencies to avoid pulling in unused ssl libraries
2bc747aaea openvpn: reduce binary size using --gc-sections on linking
e6871ab925 openvpn: fix disabling DES support in mbedtls
13592c1454 openvpn: update to 2.4_rc2
f67867adb0 vti: add empty install rules for vtiv4 & vtiv6
5ab258e57a gre: add empty install rules for grev4 & grev6
6c82f8a483 uqmi: add plmn set functionality for netifd proto handler
363c3e68ac adb: new package "Android Debug Bridge"
c8043137bb ramips: Add support to TP-Link Archer MR200
190ee7d86b ramips: add support for ZyXEL Keenetic Omni / Omni II
83eca5d8b7 comgt-ncm: fix typo Fix typo in ncm.sh. Resolves:
3561d89ad6 ar71xx: RE450: enable building of TP-Link RE450
9c475eca3e ar71xx: add support for TP-Link RE450
236fc232bb ar71xx: sort items in 11-ath10k-caldata alphabetically
5515edae9f firmware-utils/tplink-safeloader: add support for TP-Link RE450
0d9d980ecd firmware-utils: kernel image generator for TP-Link RE450
87b0747263 ath10k-firmware: fix missing variable renames (FS#341)
324bdf3ecc ar71xx: remove redundant -j from TL-WR1043ND v4 kernel build command
00dbfa1764 odhcpd: Use procd_send_signal in odhcpd-update file
05abcf518d hostapd: update to version 2016-12-19
e5e98d58f7 ncurses: set ABI_VERSION to avoid running into rebuild issues
4e138663c6 Revert mirror hash fixes
8515deb60a ath10k-firmware: bump qca988x version
7acb7dc3db ath10k-ct: Enable DFS when "Enable DFS support" is set for kmod-ath
4344eb62bf mwlwifi: select 802.11ac support
2d4c42ad49 mt76: select 802.11ac support
84daeb2e14 ath10k-ct: ath10k-ct specifies that it supports 802.11ac mode
8f3d8c0022 mac80211: ath10k specifies that it supports 802.11ac mode
77ece30eb9 hostapd: Add ability to specify that that wireless driver supports 802.11ac
842ed8448d kexec-tools: remove useless CONFIG_KEXEC_TOOLS_TARGET_NAME indirection
fe4fe3edf2 kexec-tools: build by default, even if CONFIG_KERNEL_KEXEC is unset
ff47fb0dd9 kexec-tools: enable support for x86_64
1a071115d6 kexec-tools: update to 2.0.14-rc1, fix build errors
364ec6e0e0 kexec-tools: fix compile error
81a2f9d6f8 target/linux/x86/image: add explicit prefix to grub-mkimage command
65c8f2890c grub2: upgrade to 2.02-beta3 (3 years newer than previous)
77812cdfec grub2: disable 'check-macro-version' build rule in 'po' build
2b54fa4dff grub2: do not generate mkfonts at build time
b33845b2da grub2: add PKG_FIXUP:=autoreconf
f628d0e0e9 hostapd: update to version 2016-12-15
1a4d07c2c5 ar71xx: add support for TP-LINK WR1043ND v4
51740990cd firmware-utils: add support for TL-WR1043ND v4 to mktplinkfw and tplink-safeloader
0495181529 ar71xx: rename mktplinkfw-initramfs to more generic mktplinkfw-combined
fff6443b5b firmware-utils/tplink-safeloader: refactor code for further board support
d58e8a9076 firmware-utils/tplink-safeloader: make vendor data optional
c21af889bb brcm2708: unbreak the spidev build
87522a7bf2 linux: drop deprected hifn795x patch
4f874423fd usign: fix mirror hash
9ee74b5753 ubox: fix mirror hash
bf6f4bfad1 opkg: fix mirror hash
cbca3ae92e libs/cyassl: re-enable the stunnel flag
f7319244cb linux: drop HSO support patch
bbe825c74d procd: update procd.sh to support sending kill signal to a service
d700c120bf ipq806x: EA8500 fix sysupgrade over stock firmware
96a7ee3c80 ramips: adding registration for si3210
b522292405 base-files: add support for overlaying rootfs content
3c1f20d0bb libnl-tiny: define _GNU_SOURCE if not defined
4e1f7ad56e kmod-sched-cake: diffserv3 & change defaults
197b11f325 iproute2: tc - update cake support
305704f405 mediatek: enable support for vfpv4 and neon
15734b023b libs/cyassl: Enable multithreading, drop stunnel
79abb8f140 kernel: bump to 4.4.39
6a902108a8 libs/ncurses: update to 6.0
6b08a47263 kernel: add support for Option Fusion+ PCMCIA card
d2da2c2cb3 kernel: add support for PD6729 PCMCIA bridge
04f29eef37 firmware: add support for PCMCIA Aircard's
676a11d710 kernel: enable CONFIG_PCMCIA_LOAD_CIS
87bc410f7c kernel: declare AddDepends in pcmcia.mk
a7cacc9735 kernel: don't load pcmcia_rsrc in kmod-pcmcia-yenta
1599a14b32 uboot-envtools: drop executable file attribute from files/ipq
a9ce2ba31c uboot-envtools: fix Edimax BR-6425 board name
35ed3be59f uboot-envtools: fix code formatting style in uci-defaults files
f70a2adca1 uboot-envtools: keep boards in alphabetical order
600d648a0d uqmi: Prevent 'POLICY MISMATH' error.
4146047eaf uqmi: bump to latest git HEAD
02ca833f04 ramips: WNDR3700v5 fix mtd partitions and radios
6439e39677 uqmi: add support of using device symlinks.
13ab314b0b comgt: add support of using device symlinks.
cf62a17710 hostapd: remove never-used Package/<name>/Description
ef94b9d08e mdns: bump to latest git HEAD
f145a64fb6 mountd: update to latest git HEAD
2b510d97ba tar: fix reproducibility issue
dea6baf8fa usbutils: fix download filename
a032940bfb Revert "ath9k: Add airtime fairness scheduler"
47bc081e76 ath9k: Add airtime fairness scheduler
b3a871dd3d mac80211: backport "cfg80211: limit scan results cache size"
00bc7f0357 mac80211: merge a number of minstrel/minstrel_ht performance and memory usage improvements
6f77b8d510 odhcpd: Bump to git HEAD version (various fixes)
78a1b6e880 scripts/update-package-md5sum: remove file, it is obsoleted by make check FIXUP=1
180e93ba8b build: add CHECK_ALL variable to allow make download/check to include not selected packages
d49059693b build: add FIXUP option for make check
7a315b0b5d build: implement make check and make package/X/check
720b99215d treewide: clean up download hashes
4921760a45 ath10k-ct: Update to latest CT ath10k driver.
7d760284a7 odhcp6c: Pass parameters to user dhcpv6 script
44ac4adb34 map: Have cmake find libubus.h
6a5cc2d085 include/package.mk: sync default value for hash fallback with mirror hash
881c5b47ec build: remove duplicate Download/default definition from include/host-build.mk
651bc94df4 download.pl: check for existing file before the first download attempt
f3b866f93a ath10k-firmware: fix typo
3a1e3b4e0d package/kernel/linux: only access kernel config if DUMP is unset
7747fac375 ath10k-firmware: untangle CT firmware filenames, fix conflicts
7416d2e046 build: replace MD5SUM variables with HASH
aada15af93 ar71xx: add support for TP-LINK TL-WR940N v4
93227e4d3f dnsmasq: fix service reload
a2798cff0f realview: drop the target
44ecfc26eb armvirt: new target
fb237477fd mt76: update to the latest version, fixes a build error on some platforms
4cc1f1ac1c x86: revert default root size back to 256 MB
fb74550bdf odhcpd: update sha256sum
e0b8b24cfb base-files: fix CONFIG_VERSION_DIST default
a4232cd4bf build: use SNAPSHOT instead of CURRENT to designate untagged branch builds
98b14e0906 ar71xx: fix TL-WR842N v2 switch port order
21cb84435a ar71xx: Added missing support for Linksys E2100L
38ebd1d133 firmware-utils: add E2100L support to addpattern.c
3494ca66c5 linux: do not autoload sdhci.ko as sdhci-pltfm.ko already depends on it
fc6ed9521d brcm63xx: image: trim revision code used for --rsa-signature
b4aa3c899c ipkg-make-index.sh: drop a few non-essential fields
34c2b3de66 ipkg-make-index.sh: drop md5sum from package index
970dd4dd58 kernel: netfilter: split out iptable_raw into a separate package
565988ab47 gcc: rip out transactional memory related bloat from crtbegin
e82c8d6e20 swconfig: replace the shared library with a static one
e175a4d4f1 ppp: use --gc-sections to save a tiny bit of space
4297f4f901 libs/libpcap: update to 1.8.1
28f6951600 ath10k: fix a soft-lockup on firmware restart
7dcccacb98 ath10k: fix a bug on sending null-func frames
70011393a9 ath10k-firmware: removed broken submenu
1e15d92de1 kernel: add a missing submenu
5bd3b9dfc0 comgt-ncm: Add support for specifying profile index
2e2748b053 uqmi: Add support for specifying profile index
866b7bad00 dropbear: clean up default PATH handling in makefile
132b88ea39 ramips: adding DWM-158 3g Modem
fd62fa752b ar71xx: Add support for Netgear WNR2000v1
c9a9f9b8ce ar71xx: Add ath10k-firmware-qca988x for DomyWifi DW33D
b22a20af45 procd: add support for service signals
e2f8d200f5 netfilter: drop proprietary xt_id match
2daab45cae firewall3: drop support for automatic NOTRACK rules
a6781ef4c1 kernel: kmod-hwmon-tmp102: add dependency to kmod-thermal
a7c2310278 odhcpd: Fix dnsmasq re-reading hostfile
942904f7b9 dnsmasq: Specify directory /tmp/hosts as argument for --addn-hosts
66482e179b ath10k: fix DMA allocation issues
57f7f91f0c mac80211: refresh all patches
4872c36c55 ath9k: add a RCU related bugfix
1b9a39c528 download.mk: improve download tarball reproducibility
19d3b78304 download.mk: remove code duplication in $(TAR) call
dbbfd41118 download.mk: use $(error) instead of a regular shell error
d6ef917bdb kernel: backport ubifs support for dirty_writeback_interval
2ca4c74279 bcm53xx: backport missed BCM53573 ILP patch from 4.10
f5b833b8fe kernel: bump to 4.4.38
1feb166ee7 bcm53xx: backport DTS patches accepted for 4.11
88f8c8d7eb iproute2: support latest cake & restore DSCP washing
1f0ff783f0 kmod-sched-cake: update & restore DSCP washing
d1a2c3f9b1 firmware-utils: tplink-safeloader: update support lists for CPE210/510/...
fcf54f79d2 ar71xx: simplify model detection for TP-Link Pharos devices
b305b8c386 mt76: update to the latest version, fixes dfs issues
b9ddf3098b tcpdump: reduce size of -mini by removing more infrequently used protocols
a4a00d794f net/utils/tcpdump: update to 4.8.1
64590f3c7e mbedtls: tune config to reduce size and improve performance
732c24a0ca mbedtls: sync with polarssl config
a456dd96e7 openvpn: quote parameters to --push in openvpn config file
4b8c69258e mbedtls: enable MBEDTLS_DHM_C
8f23ec609c ar71xx: remove obsolete flash chip locking code
a5923cd549 ar71xx: remove PB92 reference design board support
30285facbe ar71xx: remove AP113 reference design board support
4c8a9b8e39 ar71xx: remove AP81 reference design board support
fd95dec2e3 ar71xx: remove obsolete duplicate driver source file
441ee62931 ar71xx: remove AP83 reference design board support
fa04682f21 ar71xx: clean up spi controller related patches
52c7375c13 bcm53xx: disable CONFIG_FW_LOADER_USER_HELPER_FALLBACK
6b94234a65 lantiq: remove "init" kernel command line parameter from bootargs
4995c64857 lantiq: specify console using stdout-path instead of cmdline argument
c40477519e uboot-envtools: add support for YunCore SR3200 and XD3200
c198ca682c ar71xx: add support for YunCore SR3200 and XD3200
6ae71708c9 ca-certificates: update to version 20161130
ad907e1c03 layerscape: add 64b/32b target for ls1046ardb device
76fa771a78 layerscape: fman-ucode: prefer github over git.freescale.com
d5fc7430ca layerscape: uboot-layerscape: prefer github over git.freescale.com
b0ac825884 base-files: Changed UCI variable name for GPIO value from 'default' to 'value'
7c47f43fe6 lantiq: falcon: remove bootargs-append
4dbdba36f8 kernel: add TI tmp102 and tmp103 temperature sensors
c058f4f22d kernel: add KERNEL_DEBUG_PINCTRL and KERNEL_DEBUG_GPIO
9791fb2ac2 build: support adding version code to file names (FS#323)
ee5a6c1041 lantiq: simplify ath9k eeprom extraction script
afa3709266 lantiq: fix ath9k EEPROM data swapping for some devices
ee55a19a61 bcm53xx: update patch adding fake USB doorbell
4fbd3aa278 dnsmasq: Fix splitting hostid for DHCPv6 static leases
0422f8bcec kernel: backport LED patch which will allow better DT integration
4b3f9bc28d kernel: fix potential crash in usbport LED trigger driver
9c5af2489a ar71xx: fix LEDs and sysupgrade support for TL-WA801ND v3
a245772291 tools/upslug2: add SHA256 hash to use mirror tarball
854459a2f9 dnsmasq: reload config if host name is modified
960c477432 ramips: Fix led init script for Lenovo Y1/Y1s
011f2c26f1 brcm2708: update linux 4.4 patches to latest version
4257f6548b brcm2708-gpu-fw: update to latest version
758ef7aa99 kernel: bump to 4.4.36
8cb476c853 libs: libnetfilter-queue: update to a newer version in git repo
898857f77a ppp: Split the ppp-up for the IPv6 part
1a63b81965 orion: make image size errors non-fatal
0917999396 orion: Enable CONFIG_MV_XOR
2cb90461c8 orion: Add uboot-envtools in the default package list
7e38cd7a8d kernel: Add missing kernel config symbol
0d5097036e orion: Set appropriate DEVICE_TYPE for harddisk target
3043a4f520 orion: Switch to kernel 4.4
01bda7f05f orion: Advertise support for RTC
3ca46aa257 orion: Make sub-targets augment FEATURES, not re-define it
5763e438f6 kernel: add kernel package for the rs5c372a rtc module
a909a5d676 orion: Build images for Buffalo Terastation Pro II/Live
da5155b1a5 orion: Add support for 4.4 kernel
cec7e661e7 orion: Fold DT2 setup files into patch
9a08c0ba80 include/kernel: Switch to git download method
b9aab34eb4 include/download.mk: Allow specify DownloadMethod specific options
832fb99da2 kernel: Add check to of_scan_flat_dt() before accessing initial_boot_params
b3c5db79eb kernel: Fix alloc_node_mem_map with ARCH_PFN_OFFSET
2135e54c00 ar71xx: set GPIO reset line for Ubiquiti NanoStation Loco XW
106a4605c8 ar71xx: add support for configuring at803x PHY GPIO reset via platform data
feb25f1a5b kernel: add support for the AT8032 PHY
06a21e12ee kernel: backport some upstream at803x fixes
566de813c3 ramips: prevent packet forwarding on mt7620 between switch ports during init (FS#103)
81b5e8e5d2 base-files: add a hint in sysupgrade that shows what to do when the image metadata check fails
377eac0ceb ramips: fix LAN port order of WeVO W2914NS v2
23b58f8acb ramips: fix PBR-D1 button definition
2e020e2cef ramips: add support for PCI based OHCI/EHCI support for F5D8235 V1
13c0d208b2 ramips: introduce CONFIG_PCI and CONFIG_OF_*PCI for rt288x
c2ed721e89 ramips: improve F5D8235 V1 support
62e4c915ee mvebu: fix sysupgrade for Linksys WRT3200ACM
c95e4e715d mvebu: fix image validation error
d9d838bc97 lantiq: fix image validation errors
abedd718aa cyassl: update to wolfssl version 3.9.10
7e6c53dac9 valgrind: update to 3.12.0
4e07167eff curl: update to version 7.51.0
99ea26883b mbedtls: update to version 2.4.0
280fdac18f polarssl: update to version 1.3.18
a642a11fac scripts: getver.sh: append Git short hash to revision
5f3c96c285 build: adjust version number handling
1947cf36ba procd: update to the latest version, fixes killing jailed processes
a2e197d972 libubox: update to the latest version
7c809f1687 ramips: fix sdhci support on mt7621
0b3b8c83c0 tools: cmake: fix compatibility with LibreSSL as well
07b571a435 ramips: RB750Gr3: Add pwr LED and buzzer to DTS
fef6a96d9e ipq806x: add thermal sensor driver
2b71f958b1 ipq806x: increase coherent dma pool size
8fca99266e ipq806x: add enable reg and masks for PRNG
94e4ee5395 net: ar8327: modify some configuration of switch
5a69f59602 net: ar8216: address security vulnerabilities in swconfig & ar8216
a3454d1929 net: ar8216: prevent device duplication in ar8xxx_dev_list
eb049d3777 net: ar8216: hold ar8xxx_dev_list_lock during use_count--
65b20d8b64 net: ar8327: replace sprintf() by scnprintf()
9aa734f8f5 net: ar8327: remove unnecessary spinlocks
7de8d5322e net: ar8216: sync mib_work cancellation
550f71ec8d ipq806x: refactor rpm clock controller patches
83697ec389 tools: cmake: import another upstream commit for OpenSSL backwards compatibility
b2443838e6 kernel: add missing config symbols
7abd011b0a tools: cmake: import upstream patch for OpenSSL 1.1.x compatibility
4d448cf720 xtables-addons: add CONFIG_NF_CONNTRACK_MARK=y to all kmod-* packages
4596f9b5ac e2fsprogs: avoid picking up incompatible libcom_err.so
e678c9f764 mkimage: fix openssl 1.1.x compat fix with libressl
70b104f98c tools: mkimage: fix build with OpenSSL 1.1.x (FS#182)
f2010b0929 rtc-rv5c386a: fix include path for bcm47xx_nvram.h
59261cbf38 docs: remove all refrences in Makefiles/scripts
d52676d1ea base-files: add a wrapper for init scripts in profile
102cb4742c kernel: bump to 4.4.35
882f4d2d63 docs: deleting docs because they are obsolete
c0e66478b5 lantiq: drop obsolete patch
36148d923b uboot-lantiq: Add BT Home Hub 5A support
0e34459e6b lantiq: use BT HomeHub 5 Type A OEM partition layout
860210c373 lantiq: backport kernel patch to pass of node to nand_dt_init
62a347b1d9 lantiq: drop ath9k device tree binding & ath9k pci fixup
a20616863d lantiq: use ath9k device tree bindings binding/owl-loader
448b9b67e1 kernel: mac80211: disable ath9k bands via device tree
3f889418a5 kernel: mac80211: add pending ath9k EEPROM swapping patches
1847248fc1 kernel: mac80211: backport ath9k device tree support patches
a15ea362d7 ar71xx: fix syntax error in /lib/ar71xx.sh
9a5801e7f6 ar71xx: add model detection for UBNT Rocket Ti
9f109876ea kernel: have kmod-ipsec depend on kmod-crypto-echainiv
a07c4977ac brcm47xx: fix initramfs image build error
f12f77b477 brcm47xx: merge cpu cache workaround patches into one, ensure they get compiled out on mips74k
1cd7ff3e96 ar71xx: remove squashfs-64k rootfs image from bin directory, the generic one is enough
eff858e8df ar71xx: remove split kernel/rootfs images where the sysupgrade image can be written to flash directly
cc550d0005 ar71xx: remove 2MB flash variant of WP543
12e2beaaed ar71xx: remove legacy devices that cannot be supported due to kernel partition size limits
35dda35114 ar71xx: remove legacy gzip images
88f6f0120d ar71xx: remove obsolete jffs2 image building code
e8fe83e1be iw: drop TX power patch that is part of upstream version now
480473337d kernel: use upstream accepted bcm47xxpart parsing fix
32875a2d79 bcm53xx: use upstream accepted fix for ARM core aborts
cb7ab730c7 firmware-utils: replace md5 code with Alexander Peslyak's implementation
9371542783 lantiq: add Falcon support
5cdbc86329 lantiq: add swconfig to the default packages
57d36e5bdd ltq-hcd: drop package
d561b2f5ce gpio-button-hotplug: add more buttons
18c64f41c7 treewide: fix button keys codes used in dts
4780e7e994 ramips: add size checks/append metadata where missing
6cc0ae27b9 ramips: fix Airlink AR670W factory image
7cc0d8b3bd mvebu: fix typo in image metadata support
3228c2a682 ipq806x: more dts cleanup
e3caadc69d ipq806x: clean up dts files
97eff5cba5 firmware-utils: Fix build failure in mkmerakifw.c FS#298
04a76da1ae ipset: Add InstallDev to provide libipset as library
d76ee5bfac lantiq: specify the PCIe controller's interrupt, size and address cells
79741dc379 lantiq: Register the device tree node with the PCIe controller
c723646f22 ramips: Add missing chunked-io directive to W2914NSV2.dtsi
a7de18718d ramips: SamKnows SK-WB8 DTS cleanup
bbdb20f649 kernel: fix typo in input-gpio-encoder package title
2c05fd7ef4 tools/cmake: update to 3.7.0
a22464b92f tools/quilt: update to 0.65
a6e790b202 tools/scons: update to 2.5.1
95e7868e7e Revert "mvebu: simplify etc/board.d/02_network"
ee6beb2e1c ramips: remove kmod-ledtrig-usbdev from recently added devices
6998b8a054 ar71xx: move DomyWifi DW33D to nand subtarget
ae79c41286 ipq806x: add support for TP-Link Archer VR2600v
0e7869f204 remove bogus dev/null that was accidentally introduced while applying a patch
23a55102df kernel: remove another redundant KCONFIG entry in virt.mk
d5c3a7b1ab kernel: fix virtualization kmod dependencies and kconfig symbols
e57bed5bc3 kernel: remove kmod-vhost_net, fixes build breakage
f3096e6322 sunxi: enable CONFIG_VHOST_NET like on x86
28cd4880a5 kernel: add missing config symbols
a9dce48b22 libnl-tiny: Remove GENL_ID_GENERATE
715fd8c5bc target: sunxi: enable builtin crypto-hw module sun4i-ss
f66cb6f810 build: find_md5: ignore non-existent files or directories
49856a4bb5 apm821xx: make it possible to update the dtb partition on the WNDR4700
468735c3a2 target: sunxi: enable kvm support
d206dfdf35 package: add kernel packages for kvm virtualization
49703b589b toolchain: gcc: disable ifunc on *-musl by default
62da60b220 build: scan.mk: remove not used variable SCAN_STAMP
426e4d93bb uml: clean up the kernel config and add squashfs+ext4/f2fs support
4081333084 package/utils/fuse: update to 2.9.7
539ae47103 mvebu: simplify etc/board.d/02_network
9fc0bcdd18 mvebu: use image metadata for firmware validation
d596c21ebd lantiq: write protect vgv7519 u-boot and u-boot-env partitions
9720185820 uboot-envtools: make it not shared
ea12a80276 uboot-lantiq: vgv7519 fix tftp loading of big kernel/image size
ec1de9b1a6 ramips: Add device DLINK DWR-512-B
8f561c6516 ramips: do not append metadata to CY-SWR1100 factory image
f1d0eba3ea ramips: cleanup dts files of mt7621 based boards
18e7f49975 ramips: order mt7621.mk alphabetical
4592067a24 ath10k-ct-firmware: Update to latest firmwares.
f94bee8c02 ath10k-ct: Update to latest.
4da8bde638 netifd: update to the latest version
d2b79e4d80 brcm63xx: Livebox 1: add userspace board support
aedca3ce43 brcm63xx: Livebox 1: relocate the kernel to fix boot
422ba32c71 brcm63xx: Livebox 1: fix part probe name
768595c9f1 brcm63xx: Livebox 1: fix led naming
727ebf3a70 brcm63xx: Livebox 1: use button 1 as failsafe button
48cfc826eb base-files: ignore failure of stopping services on removal
88a14bfd1d opkg: run prerm scripts for the old version also on upgrade
afaa34ccd7 base-files: don't modify enabled state of service on upgrade
a58f176ef2 opkg: set PKG_UPGRADE also when running scripts for the old package
3c52cbfa53 Revert "grub2: add PKG_FIXUP:=autoreconf"
fe43d90d93 ramips: fix wrong check for MT7621AT
c2582f58dc lantiq: add missing metadata for tp-link images
bf3d92f0cd scripts/getver.sh: treat all commits as local if can't find upstream
a0ea22ac43 grub2: add PKG_FIXUP:=autoreconf
605cab749e ramips: Fix sdhci kernel panics on MT7621
320d8fa3bc odhcpd: update to latest git HEAD
41164ba2dc odhcpd: update to latest git HEAD
8aa9f6bd71 mvebu: Add BQL patch for mvneta driver.
a72e1692b8 firmware-utils: Add support for the Cisco Meraki MX60/MX60W
ffd7c15500 lantiq: use dwc2 by default on danube
6f60926bab lantiq: dwc2 parameters for danube
5c06a31e23 lantiq: device tree bindings for dwc2 on danube
c82d5b30e1 lantiq: initialise dwc2 on danube
f478ec2007 apm821xx: Add support for the Cisco Meraki MX60/MX60W
68634426fe ramips: add support for WeVO W2914NS v2
a74394be00 openvpn: update to 2.3.13
39433bb618 ar71xx: Fix switch config on Mikrotik RB450/G
d6e8b1f841 uboot-envtools: add 'dockstar' for kirkwood
d86f08cc94 uboot-envtools: add support for YunCore CPE830
e33dcd1cfe ar71xx: add support for YunCore CPE830
dcceea4fd3 uboot-envtools: add support for YunCore CPE870
eb9ba2b91e ar71xx: add support for YunCore CPE870
9ee8257cc7 uboot-envtools: add support for YunCore AP90Q
01dda0659e ar71xx: add support for YunCore AP90Q
16afa08d19 ar71xx: add support for COMFAST CF-E380AC v1 and v2
31952dbd1c ar71xx: add support for COMFAST CF-E320N v2 and CF-E520N/CF-E530N
c380772c19 ipq806x: c2600: change wan and lan led trigger to swconfig port
8b1731964b ipq806x: enable swconfig LED support
23e0b08a77 kernel: remove pipetypes unused var warning
70434c3f94 ipq806x: switch to upstream usb driver and backport fixes
6e65576f2d ar71xx: fix drivers/mtd/nand/ar934x_nfc.c
16adf49620 lantiq: remove device specific sysupgrade image checks
b5ee86c4e5 ipq806x: remove device specific sysupgrade image checks
0d3be662ce firmware-utils: tplink-safeloader: keep per-device info on trailing char
746e63201b kernel: add bcm47xxpart patch fixing parsing with some TRX formats
27c355f8a4 ipq806x: fix build errors
369317ce48 kernel: rtl8367(b): fix build error
7738227321 lantiq: run append-metadata before check-size to fix build errors
81e3c022e0 x86: fix GRUB_ROOT for Xen subtarget
478f1f6b16 ramips: append metadata to images
be296745f8 lantiq: append metadata to images
9d6d7d9a0e ipq806x: append metadata to images
77265e00c7 build: add support code for appending metadata to images
cc853810a4 base-files: validate metadata of sysupgrade images
929641fa1f fwtool: add utility for appending and extracting firmware metadata/signatures
5e339a48aa bcm53xx: build image for TP-LINK Archer C9 v1
2d61c26f02 bcm53xx: support SafeLoader format in sysupgrade
222783c65c firmware-utils: tplink-safeloader: add Archer C9 support
1c6fd8c1ee osafeloader: new util for extracting partitions from SafeLoader
eab2b17d43 bcm53xx: add kernel support for TP-LINK Archer C9 V1
fd924d2068 firmware-utils: tplink-safeloader: use one function for generating images
ea249f01b1 firmware-utils: tplink-safeloader: add struct device_info
5dd13c071b ar71xx: enable serial console on mikrotik devices
348344874c ramips: add support for ZyXEL Keenetic Viva
a4814c744c firmware-utils: add tool to create zyxel images
4545a60edb kernel/modules: add kmod-switch-rtl8367b
5f38d1ad85 ramips: add MT7620 MIB support for switch and port
8459d85fa3 ipq806x: refresh patches
d723f2573a libnl-tiny: remove include/linux overrides to fix various build issues
3d680c5728 ramips: add support for Sitecom WLR-6000
8b65fef173 ramips: add support for Digineo AC1200 Pro
6e3d7897f7 ramips: cleanup ZBT-WG3526.dtsi
efbb654f6c ramips: split ZBT-WG3526.dts into dtsi and dts files
9db46da8d7 kernel: enable pcrypt
16faf4aeaa octeon: fix feature flag for initramfs support
c18bf14dab hostapd: fix PKG_CONFIG_DEPENDS for CONFIG_WPA_SUPPLICANT_*
8e47655d4e kernel: update kernel 4.4 to version 4.4.32
c437a67152 devel/strace: fix build only on powerpc arch
0d760bfba8 ar71xx: tl-wpa8630: Use dynamic parsing of the firmware partition
5aace5a5fb ipq806x: fixes for R7800 and C2600
3ac5eb9141 ipq806x: fix Netgear R7500v2 memory
bb8f5162fd ipq806x: fix pci pins
84781cb6dc ipq806x: add vlans during switch init into R7800 DT
77b6bfc2f5 ipq806x: add support for RPM message RAM
07d0c1b947 ipq806x: add support for RPM clock controller
506dc815b9 ipq806x: add CPU idle states
793d448a51 ipq806x: backport upstream wdt driver
4a6f9fc633 layerscape: uboot: using perl script:byte_swap.pl to replace tcl script:byte_swap.tcl
8565630e14 lantiq: add tapi/vmmc to VGV7519 defaults
0ce929228a lantiq: enable VMMC for VGV7519
4649a92901 lantiq: disable VMMC_COEF for non FALCON device
904a6751b6 lantiq: add tapi/vmmc to VGV7510KW22 defaults
fe9a757984 lantiq: enable VMMC for VGV7510KW22
ef258a0a41 arm64: boot-wrapper: Add mirror
4162a7eba6 layerscape: ls1012ardb: only reserve ext4 fs as default firmware.bin
10889d3ebe layerscape: ls1043ardb: add pad-rootfs to reduce the size of firmware.bin
d5e84ca30f package/firmware/fman-ucode: Use HTTPS
1531c9d340 package/devel/trace-cmd: Add mirror
3bbc3bd1bd kernel: update kernel 4.4 to version 4.4.31
7ee6ab1a31 ar71xx: Add usable, inactive LEDs on OpenMesh devices
84d57fc485 mac80211: Make wlcore platform-independent
0165203304 ar71xx: add support for Buffalo BHR-4GRV2
40a16fec6a x86-generic: add MMC support to boot off SD cards
cf8aa18040 x86: add PATA support to generic and 64 subtargets
fe6a3415e0 x86: refresh generic subtarget config
5247ac2f80 ar71xx, ramips: reduce CPU load and flickering on devices using rsslieds
7ef0d7c4fc ar71xx: enable HSR tuner on Ubiquiti UAP Outdoor+
60983a486c ar71xx: fix DEVICE_TITLE for Ubiquiti UAP Outdoor+
fa845e9978 ath9k: add support for the HSR tuner of the Ubiquiti UAP Outdoor+
a250556d27 ath9k: fix ath9k_hw_gpio_get() to return 0 or 1 on success
e58f3f515f odhcpd: Add reload support
728ab77d3d ramips: fix polling switch interrupts
3d0e965c8b ramips: add port index in switch config for buffalo WHR-* and WSR-* devices
1a1c3c690f bcm53xx: add switch config for Buffalo WXR-1900DHP and WZR-1750DHP
ecab500232 lantiq: fix port indexing for WBMR-300
4cdbc90a37 ramips: add hack to detect missing mt7621 cpu cores
913219e6fe ubox: update to the latest version
a17872ec4f ramips: fix status LED for WHR-300HP2
32cfd3bd50 arptables: bump to 2015-05-20
dc7c9f590a conntrack-tools: update to v1.4.4
32f8b36d59 libnetfilter-conntrack: update to v1.0.6
00e0a7d600 nettle: enable fat build
0fe34d27e2 toolchain: fix MIPS softfloat build issue for gcc-5.4.0
5640986001 mvebu: revert remove of mvsw61xx device tree nodes
2b55c83e68 treewide: dts: use keycode defines from input dt-binding
77b807999d treewide: dts: use C style includes
de40d45363 treewide: dts: fix dtc compiler warnings
b9f609161d apm821xx: remove replaced netgear, wndr4700-usb dwc2 definiton
ebaa82a2ca apm821xx: consolidate apm821xx device trees files
3a112113e7 apm821xx: add amcc, usb-otg-405ex devicetree definition
07bc0d6089 lantiq: fix pci issue if mem kernel parameter is used
fc93494066 iw: fix build error caused by redeclaration of NL80211_ATTR_PAD
7aff00ab19 iw: update to version 4.9
7305b55588 iw: update to version 4.7
9cac5e8be0 ar71xx: generate region-coded factory images for TP-Link TL-WR841ND v11
998632bae2 arm64: boot-wrapper: add mirror checksum
9978a3e2ca base-files: Prefer busybox arp over /proc/net/arp alias
cc5c8f681e ramips: add TEW-691GR/TEW-692GR 2.4 GHz interface mac addresses
d8dd207ea6 ramips: use the ralink,mtd-eeprom device tree property
21d8de78dc lantiq: drop ralink eeprom handling function
7fd5171a34 lantiq: use the device tree bindings from rt2x00 driver
13208e89d0 lantiq: fix VGV7519 and VGV7510KW22 mac addresses
b6832817eb mac80211: rt2x00: add support for mac addr from device tree
e7c019c24d mac80211: rt2x00: fold patches
12a6e3cd05 x86: bump default kernel partition size to 16M
6649a172f2 Revert "devel/strace: fix build on mpc85xx target"
36cccbb283 kernel: select kmod-phy-bcm-ns-usb* from kmod-usb* for bcm53xx
462a7c0e96 ar71xx: fix kernel relocate stub parallel build issue
28955d9707 kernel: use upstreamed patch for BCM53573 support in bcm47xxsflash
113544dccf firewall: update to fix FS#31, FS#73, FS#154, FS#248
9c91335dc7 iperf3: update to version 3.1.4
0a6439154a scripts/feeds: use git rev-parse for getting revision
4f7947dab8 scripts/feeds: display "X" as revision of uninitialized feeds
4f7a0601e6 mac80211: rt2x00: add mtd-eeprom swab function
7f235df571 mac80211: rt2x00: remove eeprom filename dependency from mtd-eeprom
2516c0572e mac80211: rt2x00: improve eeprom_file property handling
b5638bb64e apm821xx: redo WAN green and yellow LEDs
524d7a7cde ipq806x: fix pcie reset gpios
4ad68fa0a2 ar71xx: tl-wpa8630: Fix kernel lenght
1b2b3cb8be ar71xx: wpa8630: change board name to tl-wpa8630
5f6e948551 ramips: Add support for Wavlink WL-WN575A3
a50243ea1f dnsmasq: Support add-mac option
bc4109845d ramips: fix  Newifi D1 profile
2cb4b267bd mdadm: move to Disc submenu
decf6b3314 yamonenv: move to Boot Loaders submenu
e4fef72244 comgt: move to WWAN submenu, fixed link
9abdeee0b7 uqmi: moved to WWAN submenu
64c386c566 build: remove stale .ipk files if package dir changes
7ee661def6 ca-certificates: update to version 20161102
dfc14bd145 kernel: add kernel module package for the DS1374 RTC
51b1d76f16 kernel: package module for the W83793 hwmon chips
519a199cbc devel/strace: fix build on mpc85xx target
862e7fb7b3 gcom: Fix  'mode' option for ncm
e2a65f4aa5 bgmac: backport small DMA fix
4fae9db765 kernel: fix bgmac regression causing BCM47186B0 SoC hangs
578f7b9c59 kernel: fix kmod-sound-core build error
2ab6aaca4d kernel: add SND_PCM_TIMER to kmod-sound-core
95ac6906aa arm64: switch boot-wrapper to working repository
347884b345 cns3xxx: fix UART resource overlap
fb504e8799 Revert "mt76: update to the latest version, adds a tx queue configuration fix"
5a37d0601a sdk: depend on linux/install
17ecd879b8 Revert "mwl8k: remove synchronous device init hack"
57fb5c08f5 include: Cortex-A53 is also an AArch64 CPU
3616666126 ipq806x: fix zyxel image build error
fcf90318c5 ipq806x: clean up the kernel config and reduce kernel image size by disabling some unnecessary code
fddd532612 ipq806x: fix a kconfig issue
6aa07b8202 Revert "mac80211: remove ath10k delayed initialization hack"
9f61ccd9e3 target/sdk: Switch to xz compression instead of bz2
8f2c2f94cf apm821xx: add back end-of-UBI marker for the WNDR4700 and MR24
32867540ea mt76: update to the latest version, adds a tx queue configuration fix
cae688544d mac80211: fix A-MSDU tx aggregation (FS#174)
db82db3203 mac80211: minor cleanup
5c11a4b311 mac80211: fix a tx A-MPDU aggregation issue
3db1a5c8fa lantiq: use external pci clock on ARV7506PW11
112cf52d45 lantiq: cleanup dts files
12bd0f2820 mac80211: replace the previous fix with a revert of the faulty upstream commit
e2fd98793e elfutils: bump to 0.167
cb037d1842 mwl8k: remove synchronous device init hack
efd9dec319 mac80211: remove ath10k delayed initialization hack
5f8f8a3661 base-files, mac80211, broadcom-wl: wifi detection and configuration
5e35b4562f base-files, mac80211, broadcom-wl: use uci to populate wireless config
ba3540db62 base-files: generate /etc/config/wireless, if it doesn't exist
f78405f500 mac80211: fix regdomain change issues with CONFIG_ATH_USER_REGD
69ace0824f mac80211: fix a minor issue in the header padding patch
4dfc0be07b mac80211: fix AP powersave issues introduced in the last wireless-testing update (FS#241)
a2944a0c09 scripts/feeds: use 10 chars for feed name column width
b2135f3ba5 ipq806x: update DT in accordance to new drivers And add some more DT nodes
681f28990d ipq806x: switch to generic cpufreq driver cpufreq-dt
a154a3d8be ipq806x: add opp patches for voltage scaling
8749fb7894 ipq806x: update clk-qcom patches
bf7166e545 ipq806x: fix leds, sata port for Netgear R7800 and minor fixes - renamed leds in correct color accordance - blink power led with white during boot and with amber when flashing firmware - fixed usb leds - enabled unused wps and rfkill leds as wlan leds. Now rfkill led is for 2.4GHz and wps - 5GHz WIFI - removed unneeded bootargs - removed unneeded pci pins from R7800 DT (driver already handles it in proper way) and add tx offsetting - nand ecc step size - fixed sata ports
5511c1c7c1 ramips: Use MT7621 I2C driver for MT7628/MT7688
08279810ed uboot-envtools: move to Boot Loaders submenu
dafbc94f95 ipq806x: TP-Link Archer C2600: convert old usbdev trigger to new usbport
faf94d926e ramips: add support for MikroTik hEX v3 (RB750Gr3)
df1804b75c dnsmasq: support log-dhcp option
2f2ea7b44c kernel: update kernel 4.4 to version 4.4.30
eefe07ef4d ramips: add usb packages into DIR-860L B1 profile
eb10b13f16 iproute2: rename ip to ip-tiny and let both ip-tiny and ip-full provide "ip"
7a58972680 uboot-sunxi: fix default config for OLIMEX A13 SOM (FS#239)
12d15fa8a5 scripts/package-metadata.pl: honour DEFAULT_VARIANT
5e0441aaf0 base-files: uci-defaults: support requesting untagged switch port configuration
317b3556a4 include: properly update .install stamp files
f64360c7ca scripts/package-metadata.pl: fix handling of virtual (PROVIDES) depends
b7f7e9fe42 include/host-build.mk: use STAGING_DIR_HOSTPKG
d7bec5609c rules.mk: add STAGING_DIR_HOSTPKG variable
fb58cd2fed fstools: add build-depends on util-linux
8cc0c34ef5 ar71xx: Add support to Powerline ac TP-Link WPA8630
15a14cf166 layerscape: add 64b/32b target for ls1012ardb device
c6c731fe31 layerscape: add 64b/32b target for ls1043ardb device
a34f96d6cf ramips: Archer C50 cleanup
7929ab60bf lantiq: add vpe/watchdog modules to kernel
a7672fa5b4 lantiq: added xrx200 as plattform for ltqvmmc
8c08ccc937 lantiq: added xrx200 as plattform for ltqtapi
4552bf158c lantiq: vpe softdog
e0229a16b0 lantiq: added support for VPE1
01ab5209c0 lantiq: modify vr9.dts to support vmmc
04cf9443c5 lantiq: fix vmmc build
29367aac42 lantiq: ltq-vmmc add support for ar9-vr9
8f7e58c0fe ipq806x: add reserved memory node in Netgear R7800
369884c2a1 ramips: Add RTC driver to kernel for working hctosys
0744b6a044 ipq806x: ArcherC2600: export usb power pins
dbf2feb2b3 ipq806x: ArcherC2600: devictree cleanup
d15dc7e85d fstools: update to latest git HEAD
a569354481 kernel: update kernel 4.4 to version 4.4.28
9e8e8b7253 base-files: sysfixtime: Keep RTC time in UTC timezone
76847c7fc9 kernel: deactivate CONFIG_QCOM_SPMI_TEMP_ALARM
12f0d5402c hostapd: properly package wpa-supplicant-mesh
6797a10fa1 hostapd support for VLANs through a file in addition to Radius.
98c86e2970 uhttpd: Add Basic Auth config
671cb35880 musl: fix parsing of quoted time zone names
53b43e65e7 ar71xx: Add net config for MR12 & MR16
7cb82d4b70 ar71xx: fix ethernet on wpj344 board
b7fadb12b7 lldpd: freeze execution of lldpd during reload
909f063066 lldpd: fix reload function for when interfaces change
ccf0648e72 ath10k-firmware: update qca9984 firmware
00d1e6c75e firmware-utils: fix compilation on MacOS X
f20ba0f0d5 brcm47xx: image: use append-rootfs step for per-device rootfs support
027b2c5b83 brcm47xx: image: make TRX steps work with rootfs passed as $@
8bd2167236 brcm47xx: image: make linksys-pattern-partition leave specific file
c9fdb23345 apm821xx: fix USB LED trigger for WNDR4700
1e3c4f763c openvpn: cacert does not exist
dc6cc04016 config: ext4: increase x86 rootfs size to 2GB to support online resize2fs
d1ae4c4958 config: ext4: drop option to set maximum number of inodes
244955de16 include: image.mk: make ext4 reserved blocks percentage optional
168adaefc2 linux/modules: drop ledtrig-netfilter
0ec48b883c openvpn: add handling for capath and cafile
bc6be3e953 brcm47xx: add support for per-device rootfs
dc8605b7f7 package/network/utils/ipset: Update to 6.30
a8b9fbee24 util-linux: disc -> Disc and moved some packages
6408ea0486 ath10k-ct: Add QCA9888/9886 support, fix compat issue.
b745bfa6dc base-files: Ensure reset only works if an overlay exists
83ece71d63 netifd: update to latest git HEAD
776aa91b0f uboot-kirkwood: fix default bootcmd for Seagate Dockstar
705240eeb5 uboot-kirkwood: bump to upstream 2016.09.01
d9c3727288 imx6: Add ds1672 RTC to kernel for working hctosys (Gateworks)
e3875350f3 ar71xx: add support for D-Link DAP-2695 rev. A1
6b0d279ca5 ar71xx: build relocate stub for generic and legacy images
e19427bd79 ar71xx/base-files: rename 09_fix-trx-header 09_fix-checksum
9dfed03c35 mtd: add fixwrgg command
dec29082e0 mtd: fix endianness detection on musl
136319e72d kernel: mtdsplit: add support for WRGG images
55eb6ed061 firmware-utils: mkwrggimg: new tool for D-Link DAP-2695
a35f9bbc43 dnsmasq: Multiple dnsmasq instances support
f2752f4735 grub2: add missing SECTION variable and remove non breaking space
311682905e ipip: Support fqdn as remote tunnel endpoint
9097dc5ad8 uhttpd: create self-signed certificates with unique subjects
82132540a3 uhttpd: prefer px5g for certificate creation
89817614bb netifd: Request DHCP option 121 (classless route) by default
86c6b07e15 wwan: rename data files
a2361eebfd usbmode: rename data files
c5a7e2c2fb ar71xx: Ignore firmware building errors of UBNT and CyberTAN devices
9275964e1d px5g-standalone: move to Encryption submenu and fix Title
7fa89d7f3c px5g: move to Encryption submenu
ebd7e565c7 package/uboot-envtools: Add support for ZyXEL NBG6817
783875f18b package/basefiles: add mkfs.ext4 and losetup binaries to ramfs list
1465bebd74 ipq806x/nbg6817: add sysupgrade support
d8059e3a30 linux/mtd: add id for mx25u3235f needed by ZyXEL NBG6817
a0ed7af6c6 ipq806x/nbg6817: add support for ZyXEL NBG6817
91b518512d strace: Update to 4.14
b760afa09a lantiq: danube fxs bugfix: changed compatible attribute of vmmc
85fbffd74b qmi: add metric, defaultroute and peerdns options for qmi protocol
35129469ca mbim: add metric, defaultroute and peerdns options for mbim protocol
72eb2b8e22 comgt: add metric, defaultroute and peerdns options for directip protocol
c560d25d19 comgt: add metric, defaultroute and peerdns options for ncm protocol
d2606107ab kirkwood: fix pogo_e02 LED name
e7dc511e64 uboot-zynq: fix compile error for be short of dtc
d140648622 grub2: move to Boot Loaders category
f9ed2bc92f fconfig: move to Boot Loaders submenu of Utilities
762928a13e rbcfg: move to Boot Loaders submenu of Utilities
8312738806 ramips: fix PSG1218 LEDs
a71a8955f2 ar71xx: add support for TP-Link WR802N v1
da1b33fc4d package/system/mtd: fix usage message
f6b5df44d9 kirkwood: remove redundant code in etc/board.d/02_network
fac018b25e ar71xx: Remove switch config for the MR12/MR16
28dd52b079 ar71xx: add mac partition to the MR12/MR16
d8662ac3c6 ar71xx: Move MR12 & MR16 from legacy to generic
7b9ac39afa ugps: update to latest git HEAD
5481ce9a11 imx6: Add ds1307 RTC to kernel for working hctosys
5528573039 kirkwood: Add RTC driver to kernel for working hctosys
7ba9a3a504 ar71xx: Add support to DomyWifi DW33D
81b256ee00 uhttpd: fix handling of special "/" prefix when matching handlers
93f9a9c71c kernel: backport MIPS's ioremap_cache from 4.5
13e6f7a75d brcm47xx: reorder older entries in image Makefile
839b657a61 kernel: add fix for CVE-2016-5195
75e63c2494 kernel: update kernel 3.18 to version 3.18.43
2fc3680dd0 kernel: update kernel 4.1 to version 4.1.34
06405df7a8 brcm47xx: bump kernel to 4.4
6e64a38b00 brcm47xx: build also TRX image for Linksys WRT300N V1
337f219130 brcm47xx: open code Makefile entries for all devices
0ec2738b21 toolchain/gdb: update to version 7.12
ecc091b0f6 binutils: remove old unused versions
3764caa934 mvebu: add support for the Linksys WRT3200ACM (Rango)
5da412bf80 mwlwifi: upgrade to 10.3.2.0-20161013
2beab73fad mvebu: add missing status LEDs for Linksys WRT1200AC and WRT1900ACv2
920f922652 kernel: update kernel 4.4 to version 4.4.27
2187f57db6 base-files: add ucidef_set_led_usbport for full usbport support
32c28a78f7 kernel: update kernel 4.4 to version 4.4.26
66d604d4a8 busybox: adjust download mirror
8cc9224115 sdk: predefine SOURCE_DATE_EPOCH
3b26a5bb15 bcm53xx: include b43 in Tenda AC9 image
70af3bfd57 libreadline: set ABI_VERSION to force rebuild of dependent packages
3c5a8a2cbc lantiq: enable cpu temp driver for all vr9 boards
23e3314cad lantiq: fix thermal sensors driver
eba84bee4c lantiq: Sanitize device tree files
72d12672de lantiq: Fix buttons for ARV752DPW
fa14124616 lantiq: use new build code for DGN3500
1f7a03a706 lantiq: drop lzma-loader
17094e9e64 lantiq: rework VG3503J image
0c3de24d92 procd: update to the latest version, fixes a few minor service handling issues
ea7462ae07 bcm53xx: include usbport trigger for devices with USB
d0b50c2770 kernel: drop usbdev LED trigger
0658527e1e switch to the new usbport LED trigger
1ffb7e47be Latest ath10k CT 988X firmware (beta-18).
536420647a ath10k-ct: Update to latest 4.7 CT ath10k driver.
81fd64df81 kernel: add package for usbport LED trigger
a92f57599c ipq806x: add back end-of-UBI marker for a few factory images (FS#228)
f5aa459043 ar71xx: Add support to TP-Link EAP120
6bb11d52f3 procd: Allow initscripts to start one daemon instance at a time
5c96200dab xfsprogs: install path consistent with fs tools
7f87f82753 kernel: update kernel 4.4 to version 4.4.25
b7b223be41 mac80211: backport some upstream a-msdu tx fixes
be7f2abb60 iperf: used an updated renamed tarball instead of main upstream URL
5f9598a432 mac80211: fix build error in ath10k with hwmon enabled
39f8e46bb4 busybox: add upstream patch to fix send_to_from
859d30d521 busybox: update to version 1.25.1
83f7ec31f8 ar71xx: set EU region code for TP-Link TL-WA901ND v4
7b6fca0e32 procd: update sha256sum
18bb1c9391 ltq-adsl-mei: fix build error
f5c741b5e0 procd: update to latest git HEAD revision
6f5f328003 scripts/freebsd.sh: Remove script
5b607bd8d8 boot/rbcfg: drop Build/Prepare rule in favor of default one
ba7cba95f2 kernel/wrt55agv2-spidevs: drop Build/Prepare rule in favor of default one
8fe09409da kernel/w1-gpio-custom: drop Build/Prepare rule in favor of default one
e09ff19752 kernel/trelay: drop Build/Prepare rule in favor of default one
9168abe8b5 kernel/spi-gpio-custom: drop Build/Prepare rule in favor of default one
7b3ba5a3a9 kernel/rtc-rv5c386a: drop Build/Prepare rule in favor of default one
ca599bb2a7 kernel/rotary-gpio-custom: drop Build/Prepare rule in favor of default one
28502a928c kernel/lantiq/ltq-*: drop Build/Prepare rule in favor of default one
f56f749d30 kernel/i2c-gpio-custom: drop Build/Prepare rule in favor of default one
a1236a30a0 kernel/gpio-button-hotplug: drop Build/Prepare rule in favor of default one
4f9c6c5235 kernel/button-hotplug: drop Build/Prepare rule in favor of default one
9f5770b81f kernel/avila-wdt: drop Build/Prepare rule in favor of default one
a24442c4f3 network/utils/maccalc: drop Build/Prepare rule in favor of default one
0af93f8f30 network/utils/rssileds: drop Build/Prepare rule in favor of default one
808a618bc4 network/utils/resolveip: drop Build/Prepare rule in favor of default one
964f8bc4e5 network/utils/owipcalc: drop Build/Prepare rule in favor of default one
d0345c6bb6 network/ipv6/map: drop Build/Prepare rule in favor of default one
3f8598feaf network/utils/iwcap: drop Build/Prepare rule in favor of default one
598722956b network/services/ead: drop Build/Prepare rule in favor of default one
8cf08b6783 network/ipv6/6rd: drop Build/Prepare rule in favor of default one
b8135a5b96 network/config/swconfig: drop Build/Prepare rule in favor of default one
8ecf7443a4 system/mtd: drop Build/Prepare rule in favor of default one
fb789c4821 libs/gettext: drop Build/Prepare rule in favor of default one
9f2ce12fff utils/spidev_test: drop Build/Prepare rule in favor of default one
ce2c6e5d24 utils/otrx: drop Build/Prepare rule in favor of default one
2b0b5824ef utils/usbreset: drop Build/Prepare rule in favor of default one
d679afa37d utils/px5g-standalone: drop Build/Prepare rule in favor of default one
8df2122cdd utils/oseama: drop Build/Prepare rule in favor of default one
4786484afd utils/nvram: drop Build/Prepare rule in favor of default one
9270ef06c6 utils/fbtest: drop Build/Prepare rule in favor of default one
832cd7ceb5 libs/libiconv: drop Build/Prepare rule in favor of default one
ab20b679f6 libs/libnl-tiny: drop Build/Prepare rule in favor of default one
58cf9a2476 network/services/hostapd: move whole files outside of patches and drop Build/Prepare rule in favor of default one
7c8c3226dc build: copy contents of 'src' folder to build dirs (if present)
02d5f9477b busybox: prevent globbing, word splitting
054f3fd57b uboot-ar71xx: make reproducible
4eb371e363 build: fix cleaning configured stamp file
c511795f47 scripts: case insensitive sort device names
5dc56b4123 scripts: add help text for some generated KConfigs
4050cfebda ramips: add support for Planex VR500.
8a2a20e71e ltq-ptm: Support 1508-byte MTU for RFC4638
cf458de382 scripts: fix build warning when overriding packages
5a922e5c41 imx6: inittab: Use login.sh wrapper so we can configure console password
636a069c42 target/imagebuilder: Switch to xz compression instead of bz2
195d2de867 package/libs/libreadline: Update to 7.0
9e87d6bdc8 package/libs/libconfig: Update to 1.5
192bf087d4 package/utils/e2fsprogs: Update to 1.43.3
ee7ef227f0 tools/libressl: Update to 2.5.0 and use mirrors
6e5de6e07b package/libs/libnftnl: Update to 1.0.6
49ee771e6b package/network/services/lldpd: Update to 0.9.5
1d7af1a296 package/libs/libtool: Switch to xz tarball
f23a44173e package/libs/nettle: Update to 3.3
913609a9b1 package/libs/libnl: Update to 3.2.28
d41e54fb02 package/libs/libmnl: Update to 1.0.4
3a136f5c56 packages/network/utils/wpan-tools: Update to 0.7
87002c0646 package/network/utils/ipset: Update to 6.29
eb16168dc7 usbutils: Switch to xz tarball, update db to 2016-07-21
c66658441b mtd: fix up error messages
098f7156cc ar71xx: add support for the Airtight C-60
e9455c561d generic: ar8216: improve ar8xxx_is_possible check
bcfb535730 ipq806x: C2600: change leds colour name
4bdf615878 ipq806x: add support for indicating the boot and upgrade state using four leds
36afaae847 lantiq: use wpad-mini for WBMR boards
335ccddc10 lantiq: fix ARV452CQW keys
bcfbeae79f ramips: use rfkill for wps button on wlan only boards
0a219c8dfb ramips: use rootfs splitter and new image build code for BR-6475ND
e7ec5df33b ramips: move edimax images to the new build code
634d690d74 kernel: mtdsplit_uimage: fix Edimax parser
35073d47bb kernel: mtdsplit_uimage: fix rootfs offset
6391af2f1f ramips: improve edimax 6200n/nl support
51bca43f39 ramips: fix edimax 6200nl switch config
bbdf2ac305 ramips: tag the CPU switch port
b35dd9584e ramips: remove fixed lan/wan interface for switch configs
c5e48abcc6 mbedtls: enable NIST curves optimisation.
f14b3705de gettext-full: update to 0.19.8.1
336e277e8b autotools: use correct version for gettext FIXUP
d42521fa07 gettext: fix whitespace
611399f1f8 brcm2708: fix image generation with imagebuilder
ad51e09fd1 mac80211: update to wireless-testing 2016-10-08
4379bcb1b4 package/devel/binutils: Update to 2.27
95a2e2c8fe toolchain/binutils: Add binutils 2.27
1341b88732 odhcpd: Upstep to git HEAD version
559fb537d8 build: use CXXFLAGS if defined
5d04dcedb4 ar71xx: move dragino2 from legacy to generic
4fc48a8cf2 apm821xx: replace recovery image for the MBL with initramfs
4104613fae kernel: ext4: Add missing kmod-crypto-crc32c dependency
d1000f81a8 x86: 64: enable pci hotplug and acpipnp
8869dd47ca ubus: update to the latest version, adds a race fix for wait_for
b306f8254f tools: add missing dependency for dosfstools
5f0965f8d2 dosfstools: fix autotools dependency
4bbc6fb7b7 tools: improve and simplify dosfstools
87b2b89959 tools: remove old mkdosfs symlink from dosfstools
db47363ff7 uqmi: re-enable autoconnect which was dropped without explanation
3b9b963e6e uqmi: always use DHCP for IPv4
5abeba3450 ar71xx: add userspace support for D-Link DIR-869 A1, generate images
594f0e80ce ar71xx: add kernel support for D-Link DIR-869 A1
e407f1a4c8 ar71xx: add back SEAMA header checksum fix (as used on ramips)
212ce6bce1 ar71xx: avoid double lzma compression of kernel for SEAMA images
0d1fb72241 ar71xx: add relocation loader
fce0b5d893 ar71xx: clean up SEAMA image build code
b81fc29123 include: prereq-build.mk: improve gcp check
0547b3ca64 lantiq: fix lantiq-dsl output spam
e6b2880276 netfilter: remove nf_tproxy_core references
4c36bcc567 ar71xx: build image for Archer C7 v2 IL
175b59c59b uhttpd: update to the latest version, adds a small json handler fix
757228b137 mac80211: update rtl8xxxu patches
7cc89af937 kernel: update kernel 4.4 to version 4.4.24
993ca3b747 lantiq: fix BTHOMEHUBV2B default packages
82b8eaa89f scripts/diffconfig.sh: fix output if TARGET_PER_DEVICE_ROOTFS is set
66a62b8966 tools: do not apply ccache dependency to xz
27950ddc0e tools: xz: force building without ccache
575d386590 tools: make all tools depend on xz
adb1566009 tools: tar: use .bz2 archive
e68c0a1325 tools: xz: use .bz2 archive
9edfe7dd13 source: Switch to xz for packages and tools where possible
34528c4807 dslite: Quote resolveip hostname argument
7694c5cf0e include: remove XZ host prereq
6638946f99 at91: Remove u-boot from platform images folder
6b31c4cb38 package: Add U-Boot for at91
eb75b6ac1f uhttpd: rename certificate defaults section
9677bfbb0f ipq806x: fix wlan mac for Netgear R7800
ec041920b7 include/package-ipkg.mk: use TARGET_PATH_PKG in Package/*/install steps
cb718eb34b include/host-build.mk: set Host/Exports for Host/Install step
4ada2fd276 include/host-build.mk: fix ACLOCAL_INCLUDE
7064a849ce include/host-build.mk: pass HOST_BUILD_PREFIX to Host/install
73c87a3cad hostapd: make -mesh and -p2p variants depend on the cfg80211 symbol
116adaa3a4 lantiq: fixup last commits
0f27096100 base-files: also generate configs when current is empty (FS#193)
7659f9ad9e lantiq: fix usb leds/trigger
e07c80dfc8 lantiq: use aliases device tree node for leds
8b639410d1 lantiq: cleanup led handling functions
dbb13a81b9 lantiq: board.d: apply alphabetical order to led file
cbc80805bd include/download.mk: Use -7e compression instead of -6 by default
ed768ae4b2 include/prereq-build.mk: Add xz-utils to make prereq
720f8eb18e ccache: disable assembler support, it breaks kernel initramfs images
4855fa35e3 kernel: fix kmod-sound-hda-core on Linux 3.18
27dc933827 zynq: fix maintainer email address
a1248daddf zynq: convert to new image build code
3c4858eeb2 uhttpd: support using OpenSSL for certificate generation
5d86dc791e include/download.mk: generate reproducable SCM tarballs
8462ec3134 kernel: add missing snd-hda-intel module for Linux 3.18 and 4.1
c34676f4d4 kernel: add missing config symbol (partial forward port of d2f4479870)
86c966a8ae build: fix regression on running make kernel_menuconfig
8a7a1b0029 kernel: add missing symbols for Linux 3.18 (like d2f4479870)
46f2ca9a8f kernel: move kmod-owl-loader to the right .mk file
4a5bab78a2 kernel: fix sound-hda-core dependency
934901fb3e build: leaving behind incomplete metadata files on cancelled builds
d2f4479870 kernel: add missing symbols for Linux 4.1
be6f836841 include: relax umask check
a69e19d18a kernel: backport usbport LED trigger from 4.9
df5416296c ramips: add support for Zyxel NBG-419N2 (WAP3205v2)
a79f3d11b3 gre: Support fqdn as remote tunnel endpoint
52974da2bb ar71xx: update kernel config symbols
c166b050fd ar71xx: base-files: fix boards order in lib/upgrade/platform.sh
8be47007a9 ar71xx: base-files: cleanups in lib/upgrade/platform.sh
92870eac27 ar71xx: comsetic cleanups in files/arch/mips/ath79/{Makefile,machtypes.h}
6e58440fc1 ar71xx: base-files: cleanups in etc/board.d/01_leds
c142df3094 ar71xx: fix LED names for GL Innovations boards
8689078a9b ar71xx: base-files: fix code style in etc/board.d/01_leds
d09f4e0631 ar71xx: base-files: combine boards with the same config in etc/diag.sh
2917ae91ec ar71xx: base-files: cleanups in etc/diag.sh
edcdb93467 ar71xx: base-files: fix boards order in etc/board.d/02_network
a75cfac1f6 ar71xx: base-files: cleanups in etc/board.d/02_network
4fa90c49c1 ar71xx: base-files: rework etc/board.d/02_network
4ef1144958 iproute2: tc cake qdisc add nat, docsis & ptm modes
de8e032385 kmod-sched-cake: update to 161002 version
15cb19f02a mvebu: fix sysupgrade
5a8a986dd5 base-files: remove non-working filter option for wifi detect
d0f17fe682 linux/modules/fs: Fix missing vfat dependencies
1fff7f2dbc package/devel/trace-cmd: Update to 2.6
ea91dda327 tools/patchelf: Update to 0.9 and remove patch
6f1d6fdbaa tools/upx: Update to 3.91 and use new tarball url
fdf200c893 tools/ppl: Update to 1.2
d88d55e0db tools/mpfr: Update to 3.1.5 and change to xz tarball
bf567363cd tools/expat: Update to 2.2.0
b8b807b1a9 tools/e2fsprogs: Update to 1.43.3
792e8bc8bb tools/ccache: Update ccache 3.3.2 and refresh patch
8a542b8516 kernel/sound: Add support for PCI HD Audio devices
dce5c4f5c8 ramips: Add support for Phicomm K2 PSG1218
a51a11931b mountd: update to latest git HEAD
5f80315634 include: add umask prereq check
b8d802fe9f valgrind: improve mips support
90a4f2ec6d valgrind: remove 110-add_a_out_h.patch
8370b9eede ntiq: make i2c-lantiqi driver compile again
ba1024b9c9 bcm53xx: use the latest XHCI doorbell patch sent for upstream
28974de663 bcm53xx: drop unneeded fix for usb3-lpm-capable DT property
d7e41df24a bcm53xx: switch to standalone USB 2.0 PHY driver
7120a43013 bcm53xx: add patch specifying USB controllers in DT
d5dcb1bf97 bcm53xx: backport BCM5301X patches from 2019-09-30
cea09329e5 netfilter: fix file conflicts between kmod-ipt- and kmod-nft- packages
c50ba61caf kernel: fix module dependency checking
7d559169c5 kernel: update to v4.4.23
949cfbb243 kernel: update kernel 4.4 to version 4.4.22
fc88eb3fdf ath9k: remove patch causing stability issues with powersave devices (FS#176)
34c2726ca7 iproute2: fix no fortify build failure
eb7307cb94 ipq806x: update Netgear R7800 device tree
71370d2c55 target/{sdk,imagebuild}: Fix for symlink-tree
c3d3111831 brcmfmac43430-firmware: remove package and switch to linux-firmware
31e0f0aec0 kernel: do not enable the unpackaged rfkill-gpio driver
0b828e3249 kernel: add missing config symbols
4aa5d3e60d mvebu: add support for SFP
a454756c91 mvebu: disable MSI interrupts
685ed1e072 kernel: add STAGING_DIR_HOST/lib to host library search path
72e9d19f6e mac80211: fix rfkill dependency
e79e555c0e ramips: Xiaomi MiWiFi Nano: fix status led
2b3b63aea3 kernel: fix build error in sign-file.c with libressl
9f6d8532c7 kernel: add missing config symbols
c795794eef mac80211: use upstream patches for rtl8xxxu
71144844e1 kernel: add missing config symbols
97c38e7f22 procd: update to latest git HEAD
76af0eff3f netifd: update to the latest version, adds various fixes
c8e68150bf toolchain: Rework external toolchain libc selection
fb586939cc ath10k-firmware: move to firmware section in buildroot
e7be0decf6 ar71xx: Do not use a hardcoded ath10k firmware mac address
3fbd235fb5 ath10k-firmware: update the qca988x firmware to 10.2.4.70.54
493b0f3f57 toolchain: Force installation into /lib
96b59dc383 kernel: add missing config symbol after rfkill change
986ec56507 rfkill: add fake rfkill support
376944c0ab perf: fix build with musl on PowerPC
82aa061251 kernel: remove echainiv.ko from kmod-crypto-iv
a0ce6982d8 mac80211: backport brcmfmac changes from 2016-09-27
68d649f5cd ar71xx: add support for Cisco Meraki Z1 Cloud Managed Teleworker Gateway
b1f39d3d7e openssl: update to 1.0.2j
142ec7ada9 ramips : add support for Newifi D1
9fe833e1d0 ramips : add support for PandoraBox D1
1bc68e1379 fortify-headers: update to 0.8
0d4f02dfd6 linux-firmware: Add mirrors
c0b15b3072 openssl: Make DTLS configurable.
aaa067ab0b openssl: Remove J-PAKE. Nothing uses it.
78ae7d8efd busybox: v1.25.0 upstream patches
edbc8fec8a libjson-c: Update to 0.12.1
509708889c libunwind: use url alias
dd1b69a058 uml: set inittab for working console
66aae9a271 ramips: Add support for ZBT-CPE102
875cddd94c iwinfo: fix WPA cipher reporting
8badcba229 iproute: properly support high routing table IDs
864b2d113a 6in4: fix invalid local variable declaration (FS#188)
45b73af7f6 mac80211: backport brcmfmac changes from 2016-09-26
5b99693832 rootfs: fail on errors in postinst scripts
021b96d7c5 rootfs: remove unnecessary and potentially harmful force flags from opkg call
593dfac909 image: per-device rootfs: first remove, then install packages
26b4216f95 base-files: make default_prerm work offline
43bf3e80b2 ramips: fix DEVICE_PACKAGES of Ubiquiti EdgeRouter X
9dbf8241c3 ar71xx: clean up DEVICE_PACKAGES of legacy devices
a16a8814ea image: don't modify file permissions before rootfs generation
6c1542787d base-files: fix check for empty password warning
77f54eae45 config: enable shadow passwords unconditionally
da4e81960d mac80211: fix crash in mac80211_hwsim
27ed4e9c14 mvebu: add switch config for clearfog pro
6859098d97 mvebu: add sysupgrade support for clearfog
c359d7e81b mvebu: add switch node to clearfog
167763837b mvsw61xx: enable SerDes on 6176 if required
92dcaecee3 mvsw61xx: reset phys on probe to enable switch ports on clearfog pro
f2102b484b mvebu: replace ClearFog dts files with patches from upstream
c4f4d65835 mvebu: enable PCA955x driver for clearfog to enable pcie and usb
c4823622d8 uboot-mvebu: reset the 88E1512 PHY to make the wan port work
d8075b15d0 uboot-mvebu: make hidden and be m for clearfog to fix IB failing to add it
bc1f006b4e uboot-mvebu: also install into KDIR to ensure it packaged in IB
997fed94e3 ptgen: work around gcc miscompilation
175fbe4d4e ramips: move /lib/ramips.sh include in /etc/init.d/bootcount into start()
b3dd642584 fstools: mark as nonshared and add missing PKG_CONFIG_DEPENDS
663145e419 image: fix CONFIG_CLEAN_IPKG with CONFIG_TARGET_PER_DEVICE_ROOTFS
ce89535bce kernel: remove duplicate br-netfilter file and Kconfig symbol from kmod-ebtables
ea288126db openssl: backport build fix when hardware support is used
524d4110f9 ar71xx: add model detection for many Ubiquiti AirMax XM devices
3675e657ed image: per-device rootfs: don't fail without opkg
e916579340 image: allow specifying additional packages for device-specific rootfs
1c09849f6c treewide: remove bad local shell variable declarations
df9efc9497 curl: update to version 7.50.3
6926325829 openssl: update to 1.0.2i
c15d70c6d6 image: don't override opkg list directory in per-device rootfs mode
d72e838429 ramips: do not "local" variables outside of a function
e9de6e5203 lantiq: do not "local" variables outside of a function
6177b649ca scripts/package-metadata.pl: fix generation of dependencies on virtual packages
4f272dd032 linux-firmware: update to current Git head
175237e7df kernel: fix broken dependency of kmod-owl-loader on kmod-ath9k
64568cac91 tools/firmware-utils: fix portability issue in mkmerakifw-old
a84d51c85d linux-firmware: update md5sum
1ac5cf7713 bcm53xx: move BCM53573 USB 2.0 patch to use backports prefix
7b472f7c21 busybox: fix md5sum
e59bbb6fe2 ltq-vdsl-app: update to version 4.17.18.6
7ecbc27951 ltq-vdsl: update to version 4.17.18.6
3a4db8548f ltq-vdsl-mei: update mei driver to version 1.5.17.6
909ed82b10 dsl-vrx200-firmware-xdsl: update to more recent versions
06fa1c46fc busybox: update to version 1.25.0
ef64c8694b base-files: Allow subtargets to define base-files.mk
e9401a2335 kernel: owl-loader for delayed Atheros ath9k fixup
7219c30da4 firmware-utils mkmerakifw-old: firmware generator for Z1
edf5b2955e cyassl: remove duplicate submenu level
b9e3e38e79 cyassl: make CyaSSL/WolfSSL more configurable
32f4777530 dnsmasq: Add match section support
559f55dffc iwinfo: Bump to 2016-07-29
dc9172b65b ar71xx: update kernel config symbols
2ad0ecc101 ar71xx: mark U-Boot and radio calibration data partitions as read-only
b9a55277d5 kirkwood: fix uimage creation for some kirkwood devices
63bd73a5cf base-files: remind users to set root password
0b3a64f862 cns3xxx: eliminate hardcoded kernel/rootfs partition split
58fbe07560 cns3xxx: move laguna.c changes out of patches, update it in files/
413eb04e1e ubifs: add full overlayfs support
41a582a986 bcm53xx: use upstream accepted ILP clk driver for BCM53573
0109ed87d9 kernel: add nlmon kernel module
8b5e128250 busybox: libnetlink: fix alignment of netlink messages
25dab5d217 base-files: reduce vm.min_free_kbytes for devices with 32M RAM
4fec58be09 linux-firmware: update to the commit from 2016-09-15
8c52fbbe3a arm64: fix build for linux 4.4.21
41eab9048b kernel: update kernel 4.4 to version 4.4.21
a530196f8d sunxi: add rtl8xxxu into pcduino v3 profile
092e77d948 rtl8xxxu: add support for rtl8188eu
c1678f1fa0 linux-firmware: rename r8188eu-firmware to rtl8188eu-firmware
f7670a2d07 mac80211: stop brcmfmac from selecting all SDIO firmwares
ba5a9aba5c brcmfmac43430-firmware: rename to brcmfmac-firmware-43430-sdio
daa5691a4d linux-firmware: separate packages for Broadcom FullMAC SDIO firmwares
01e2024754 ar71xx: set region code of TP-Link TL-WDR3600/4300 to US
b063faa2c8 ar71xx: separate TP-Link TL-WDR3600/4300/4310 profiles
fa05f1d41b kernel: fix missing rename on usb gadget kmod cleanup
88ee275562 cns3xxx: Enable driver support for onboard m25p80 SPI flash
dc17fde994 kernel: clean up usb gadget support
eb88a9cacb ramips: fix wrong blocksizes
d14c28fc80 kernel: update kernel 4.4 to version 4.4.20
65c5d097a4 mac80211: stop brcmfmac from selecting all PCIe firmwares
a3f12a8dbe mountd: update to latest git HEAD
925e63e71f ramips: enable 4K sector support in kernel config
61c2a7339a image: remove padding parameter from append-kernel/append-rootfs
14b40d61e1 image: use check-size from new image build code
1cd0a4c688 image: add KERNEL_SIZE to the default device vars
b964196c68 bcm53xx: use the latest submitted version of ILP clock driver
e70e3c544a hostapd: fix regression breaking brcmfmac
2c38b6e076 bcm53xx: specify brcmfmac firmware for every device
ac887f4832 linux-firmware: separate packages for Broadcom FullMAC PCIe firmwares
993ad29359 kernel: Backport pending appended DTB handling patches
d27bce8d28 build: drop UBI EOF marker from images by default
f3747020e2 mac80211: fix tx issue with CCMP PN generated in hardware
c7d5bc8197 ramips: improve Linksys EA8500 build code
306f1c7846 mvebu: fix OpenBlocks AX3 image
ec37a56587 ar71xx: fix typo in image build code
c1578d4fc9 cleanup ucidef_set_interface* usage
92eaf27c62 use immediate set in target Makefiles
0f6d0afa13 ramips: board.d merge redundant switch/interface configs
64d72880bc lantiq: board.d: apply alphabetical order
96f6bd501a lantiq: board.d: cleanup default switch config
7d02e94e41 lantiq: enable cpu temp driver for more tested boards
2b1c6b21b5 brcm2708: update linux 4.4 patches to latest version
ac08cb06f6 brcm2708-gpu-fw: update to latest version
591755ad1a dnsmasq: make NO_ID optional in full variant
96f0bbe91d dropbear: hide dropbear version
ca356887ed x86: disable MTD support
fe24545982 octeon: remove block2mtd support
d2a7df0792 octeon: use new ext4/f2fs overlay support
08cf46123f octeon: enable f2fs and loopback device support in the config
9d57957784 octeon: enable f2fs and ext4 utilities
3cbb7820a4 mvebu: use ext4/f2fs overlay filesystem for solidrun clearfog
bee30de984 mvebu: enable ext4, f2fs and loop device support
be59b1718d x86: drop the use of block2mtd, use ext4/f2fs as overlay filesystem
c6eb09d5a3 x86: enable mkf2fs and e2fsprogs by default
580f24bc96 x86: enable f2fs and loopback device support in the kernel config
1867537d65 fstools: update to the latest version, adds support for ext4/f2fs overlay via loopback device
d70b748942 imx6: Add static PCA953x support in kernel
7d9ef9080c ramips: set blocksize for remaining rt3883 devices
9f531efc59 ramips: remove old build code seama recipe
fb39b77ccb ramips: switch DIR-610 A1 to new image build code
bd39104e95 ramips: switch some rt3883 devices to new build code
0f3600ccee ramips: move seama build recipe to Makefile
74da44cfc2 ramips: switch DIR-615 H1 to new image build code
483fd5f6ad ramips: add build recipe for senao header
28110727f1 ramips: set blocksize for 4MB devices
05ab2323ff ramips: don't set the same max image size twice
a499d0a6b5 image: specify max image size in Kilobyte/Megabyte
e7ec7a08aa image: use k as unit suffix for blocksize
ddd259b0d5 image: pass device blocksize to padjffs2
85fefcdb61 kernel: mtd: backport Macronix sector size fix
d7b6f0ea88 apm821xx: image: add support for k unit suffix to boot-img
3e7524c184 image: add support for k unit suffix to append-ubi
b99a93ebaf image: add support for k unit suffix to pad-offset
5369a03d52 ramips: use lower case names for TEW-69xGR images
775f93e898 ramips: fix wrong TARGET_DEVICES
034c5cb820 ramips: fix wrong device title
0ac50a661b firmware-utils: mksenaofw: rework option validation
083ef3fefe ramips: add support for Mercury MAC1200R v2
943cf08fb7 oxnas: small image improvements for kd20
232767edf0 bcm53xx: enable switch port 5 on Tenda AC9
8072223347 kernel: b53: force BCM531x5 port 5 link state if enabled
dd158ef346 bcm53xx: use upstream queued patches for R8500 and AC9
29be50104e kernel: move bcma BCM53573 patch to bcma 4.9 backports
7419b9497f imx6: override default inittab to add video console tty
a2386c384d imx6: image: remove pca955x/ds1672/at24 from Ventana kernel modules
a1f83bad60 images: bump default rootfs size to 256 MB
dbbd5eef58 f2fs-tools: import from packages, clean up, and update to latest
03cd416795 dnsmasq: Don't expose *.bind data incl version
c4bfb119d8 mac80211: remove the fq-disable hack, now that reordering is fixed
a194ffd4a8 mac80211: fix packet loss on fq reordering
859d940c79 hostapd: update to version 2016-09-05
b6cd42a54e kernel: merge a softirq performance improvement patch
2728512e15 e2fsprogs: List all libraries explicitly
9a2f2f32cf e2fsprogs: Honor the global verbose flag
e9f86c6cac apm821xx: backport generic HDD led-triggers for WNDR4700 and MBL
f7c1d9c8a5 apm821xx: detect sd-card media changes for the WNDR4700
1974ad5a96 cns3xxx: add GW2386 support
1419087a35 cns3xxx: add GW2394 Support
4fd043b95b image.mk: Create a manifest file of installed packages as a build artifact
42f559ed70 kernel: backport upstream overlayfs fixes
81dfbfb069 target/toolchain: Fix toolchain packaging without package build
9209f4304b dnsmasq: fix remove pidfile on shutdown regression
c5913264e7 mwlwifi: Expose the IEEE 802.11w support to hostapd
e8cb7d30e9 hostapd: fix typo and indentation in ap_sta_support.patch
aeea251fad ath10k-ct: fix missing symbols if ath9k is not selected
49a6f67c39 mac80211: backport new register bitfield macros
9cf0444768 mac80211: add a tx sequence number allocation fix
78e63ce7e3 apm821xx: add size check for initramfs kernel for the Meraki MR24
bc36678bdb apm821xx: Fix initramfs image for the Meraki MR24
a4dc9ff934 dropbear: mdns flag is a bool, not integer
ad8d197b82 base-files: support oneshot leds properly.
b5f7221afa fstools: fix logic bug in extroot verification code
81b779d4d9 ugps: update to latest git HEAD
f362dc154d zram-swap: CONFIG_PROCD_ZRAM_TMPFS compatibility
911b6ca234 imx6: enable ARM crypto acceleration
0cf48c4407 imx6: refresh kernel config
232893037a generic: add NET3380 UDC support
3314bcf715 imx6: add GW553x support
a4b86b292a boot: kobs-ng: update kobs-ng for newer kernels
f8c7e935ef toolchain/gcc: bump GCC 6.1.0 to 6.2.0
aa53f78038 build: fix subtarget descriptions
a810e7789a oxnas: add mem=128M to stg-212 built-in cmdline for legacy u-boot
9c69ba83e2 oxnas: add method to extract mac_adr from legacy cmdline
c773a2c46e oxnas: kd20: generate image compatible with stock firmware
fe89f90119 oxnas: allow booting with legacy loaders
02a9a74d17 ar71xx: fix ethernet driver fast reset issue causing tx timeouts
358cd6d9eb ramips: fix legacy initramfs images
dbc9ee5b72 ath9k: fix regression in tx queueing patch
2d7d9baf19 mvebu: use ptgen instead of fdisk to make the clearfog image script more portable
7130833a27 mvebu: fix boot script for booting from mmc
3242c07649 mvebu: add sdcard image creation script
a67183a7bc mvebu: clearfog: require uboot-mvebu-clearfog
28a2901cba ath10k-firmware: add QCA9887 firmware
39d817cf38 Add config symbols for kernel keyring support
2d418381bb mwlwifi: Updated to latest source
a894a535ff mac80211: add fixes for dealing with unexpected BlockAck frames
372d0fea29 ath9k: add a bunch of powersave handling fixes
1e72d1bf16 mac80211: add a powersave handling fix
4f40f22fb3 Add Issue submission template (redirect to bugs.lede-project.org)
00a1056c3f openssl: re-enable ARM assembly
d3730c9aca imx6: disable EOF markers on UBI
a84a74f618 scripts/ubinize-image.sh: add support for adding custom partitions
f29774bee3 glibc: re-enable parallel builds
4badb8a023 glibc: switch to 2.24 by default and remove old versions, fixes security issues
8e0cb8f582 ebtables: fix build with glibc
18c7d1c626 dante: remove -D_GNU_SOURCE to fix build errors with current glibc
bf604f3503 glibc: add 2.24
98206cb9c6 iperf: add -lm to fix build with newer glibc
b0dcb6bfed iperf: drop PKG_BUILD_DIR override
056ce2474d x86: enable fpu for all subtargets
fa0c45c397 mvebu: add fpu to features
86e27f135b mvebu: enable ARM crypto acceleration
c419ae2da8 mvebu: enable NEON support
ef02a7154d mvebu: make MMC driver for Clearfog builtin
6f1ce6560d mvebu: refresh kernel config
8b9707379f kernel: spi-nor: add support for ESMT_f25l32qa and ESMT_f25l64qa
e9c517772c kernel: make serial port sysrq-disable patch more generic (FS#112)
bba8a1a9ba Revert "opkg: use vfork on gz_open by default (FS#120)"
d0b88b6067 Revert "opkg: disable the use of vfork for the host build"
2ca0cdb7bf ath10k-firmware: Update to latest ath10k-ct 9984 firmware.
cf76b90a5f tools: make mtools/dosfstools unconditional
fa0096f6cc ar71xx: generate US- and EU-specific images for the Archer C7 v2
a4fc62bc0e firmware-utils: mktplinkfw: add support for TP-Link's new region codes
02e3c718e9 opkg: disable the use of vfork for the host build
763f5d7873 opkg: use vfork on gz_open by default (FS#120)
3e4d0e3e77 ath9k: revert temperature compensation support patch (FS#111)
4530ca3c11 kernel: remove obsolete legacy ide kernel module packages
30d75720fa arc770: Introduce images for SD-cards
ca519d4f8d arc770: Remove MMC kernel modules, they are built-in now
cf3364a363 arc770: Update kernel configuration
07e653725a arc770: Reduce generalization
545d86490c ct-bugcheck: Add tools to poll for and report ath10k firmware crashes.
d66db35a1d ath10k-ct: Remove useless WARNING for 10.4 firmware.
3a2d142a3a ath10k-fw: Update to latest 9980 CT firmware.
1bb914dbed bcm53xx: use the latest 6th version of ILP clock driver patch
8965cf90f1 kernel: backport clk *_hw_* API for registering struct clk_hw
885910225d iwinfo: mark as nonshared
acffa62d12 mt76: update to the latest version
83997146e7 ar71xx: disable flow control to the built-in switch on AR934x
6fdc527793 lantiq: fix ath5k EEPROM loading
66f3edfd8b linux/arc*: disable MAC frame filter in DW GMAC
2b0a1292f8 uqmi: update to the latest version, adds QMI-in-MBIM support
9dc367e6f0 ipq806x: fix ipq8065 s2a/s2b regulator frequency (fixes ethernet performance)
9417293366 ipq806x: Archer C2600: Renaming LED accordance with the standard
2a64be5aa9 ipq806x: enable ondemand governor
8765c10606 kernel: backport patch for specifying USB ports/devices in DT
00e8571f2b ipq806x: rename R7800 device tree file, merge R7500v2 dts addition
212c6bd781 realview: rename config-default to config-4.4
8cba87c5bd rb532: rename config-default to config 4.1
3994f5c6fa orion: rename config-default to config-3.18
4cc2d159bc gemini: rename config-default to config-4.4
8668ce8853 arm64: rename config-default to config-4.4
2653a12c4d openvpn: update to 2.3.12
df04723478 gemini: rename patches directory to patches-4.4
012873074f perf: drop sched_getcpu wrapper
91362e7aa4 strace: bump to 4.13
58df34b5e1 gemini: drop Linux 4.1 support
f046737e92 gemini: add Linux 4.4 support
e58c20aac3 ath9k: Set ATH9K_STATION_STATISTICS when enabling debugging
d41f56864c ubus: update to the latest version, adds object remove fixes
223c124db8 ubox: move logd into ubox package
798cd261ab hostapd: use printf to improve portability.
f5860f898a build: use perl instead of GNU date for KBUILD_BUILD_TIMESTAMP
88b16da8c4 tools: build GNU date from coreutils on non-Linux systems
4170267f5a build: pass $(STAGING_DIR_HOST) to Host/Install
4c451ae0a7 ath10k-ct: Update to latest ath10k-ct driver.
b962da4d92 ramips: mt7621: switch to 24kc
a11843b62e include: remove 34k distinction
46b88b56bf lantiq: switch from 34k to 24k
8cf1d64f1c ar71xx: switch to 24kc
c487bde9e4 netifd: update to the latest version
8072264b96 kernel: update kernel 4.4 to version 4.4.19
861f566e34 brcm47xx: add missing config symbol
fcdba8d590 bcm53xx: backport patch adding ARCH_BCM_53573 symbol
277f85c21a cyassl: make CyaSSL/WolfSSL more configurable
dc765f64c5 imx6: Fix pointing to msata/mmc bootdevs
c34f953fef ipq806x: Build image for Netgear Nighthawk X4 R7500v2
d7e040f8bc kernel: add fake users for udptunnel and iptunnel modules
bb20164c8f oxnas: drop explicit pre-init iface
4eb376586c kernel: bgmac: use upstream accepted patches
c6164d9610 lantiq: fix building AVM/EVA sysupgrade images on NOR devices
00516611bd ipq806x: add usb pins to r7800 dts file
35be928466 imx6: fix generating bootfs in imagebuilder (FS#102)
c9e6b173f7 ramips: fix build of TRENDnet TEW-69xGR images
c892f37b30 ramips: move umedia build step to Makefile
bcd2113a32 ramips: TEW-691GR: fix switch and wireless
a7c6cf5182 ramips: TEW-692GR: fix switch and wireless
05912a304c ramips: rt3883: fix dtc compiler warning
63857a2d6a lantiq: generate switch configuration for BTHOMEHUBV2B.
334fdea08d archs38: Merge sd and ramfs subtargets in generic again
070edfd92f ltq-deu: fix cra_priority
9391661394 ltq-deu: fix handling of data blocks with sizes != AES/DES block size
8dba24cfc2 ltq-deu: fix aes initialization vector handling
c08651226f toolchain: include yasm in x86 toolchain
f71f7f0df1 oxnas: set preinit interface in /etc/board.d/02_network
ef4e511a81 kernel: replace cosmetic UBIFS patches with what went upstream
28d641be43 bcm53xx: update copy of ASM entry flushing whole D-cache
1bef5050ef bcm53xx: build Tenda AC9 image
5e885c09c6 bcm53xx: switch back to standalone ASM entry flushing cache
d22ae5e888 bcm53xx: package drivers for Northstar USB PHYs
f3923dab7b kernel: check the right directories for rebuild
c1f4040f70 tools: Select dosfstools for archs38
b91e58e606 busybox: enable sha256sum by default
31fada8bec bcm53xx: generate proper network config for Tenda AC9
18eebfe4e5 mvebu: fix boot stalls on WRT1900AC V1
d7c249fa1c ppp: Extend uci datamodel with persistency sypport
f478fba663 ar71xx: add support for Zbtlink ZBT-WE1526
57ef81d78f kernel: prevent adding custom string to localversion
0df2c6563a kernel: prevent addition of scm marker to localversion
1e71fca777 mtd: fix building with glibc
c8580f51ba u-boot-envtools: fix building with glibc
d7e4b9babb ipq806x: sync with latest patches sent by QCA
5e563262f1 ubox: fixes segfault inside kmodloader
27f47f6ad4 kernel: bgmac: add support for BCM53573
83f6cf649a kernel: bgmac: fix regression in MII registration
7264df3886 kernel: bgmac: backport 3 remaining small fixes
93f2aa44f7 kernel: bgmac: backport patch adding platform support
533d16822c kernel: bgmac: backport patch switching to feature_flags
df4f41261c archs38: Introduce images for SD-cards
7abf9eda8a archs38: Remove MMC kernel modules, they are built-in now
83bd1f81c4 archs38: Update kernel configuration
5f55df433d archs38: Reduce generalization
a3cde14f5a arc: use patched .dts from sources
c41506625a tools/tar: Bump to 1.29
fe7fdd3bb4 ath9k: switch to using mac80211 intermediate software queues
f2103c50ab kernel: backport bgmac patch moving MDIO code into separated file
6d3fbf2818 kernel: backport simple bgmac cleanup & fix from Jon
2803527237 kernel: add BCM53573 flash fix sent upstream
13e20e6956 kernel: update bgmac by adding Florian's upstream changes
99a1888287 swconfig: revert the portmapping patches, they seem to cause a segfault
5846620890 bcm53xx: fix warning caused by m25p80 patch
09b9dd730c kernel: support watchdog (and so reboot) on BCM53573
528b769d42 lantiq/xrx200-net: Add support for eth0 as WAN interface
2ebb4733e1 kernel: add kmod-squashfs
9f5ee6f6c0 lantiq: add kmod-ledtrig-usbdev to device packages which have usb led
a77ce8ba96 libs/gmp: update to 6.1.1
3d20f56c13 tools/gmp: update to 6.1.1
5216af7b05 tools/scons: update to 2.5.0
a247e26a7e tools/cmake: update to 3.6.1
785cdc3cf2 package/devel/gdb: Update to 7.11.1
d106c7d56b rb532: rename patches directory to patches-4.1
74aecc2d45 orion: rename patches directory to patches-3.18
d99169536e omap: rename patches directory to patches-4.4
fa5eab6ec5 au1000: rename patches directory to patches-3.18
12cdf2bfc2 malta: enable be64 and le64 subtargets
1ba88eabd5 octeon: remove the now redundant cpu cflags override
ddd1882811 lantiq/xrx200-net: add interrupt for second DMA TX channel to vr9.dtsi
8f02f7c7f8 lantiq/xrx200-net: fix "tx ring full" error by introducing second DMA TX channel
fca1eb349e swconfig: remove obsolete portmapping feature
675407baa4 kernel/swconfig: remove obsolete portmapping feature from swconfig
63f6fc5c16 samba: add file/interface reload triggers & filter interfaces
d1b20a3659 ar71xx: fix profile name of Mercury MW4530R
40b8cbc2af procd: update to latest git HEAD
d36c5152ef ncurses: change handling of PKG_CONFIG_LIBDIR
3a3424981c scripts: ipkg-build: do not require git or svn
d9345bc5bf kernel: fix crashlog on x86/64
27b078e83a bcm53xx: add quick fixes for BCM53573
38750ce739 bcm53xx: add temporary BCM53573 ILP clock driver
dd7eddcb08 bcm53xx: prepare for building Tenda AC9 TRX image
c14485d41a toolchain/uClibc: add missing config symbol
857f00a9f7 bcm53xx: drop target's preinit network support script
30352e72ff base-files: set pi_ifname in board.d case to fix deconfig
95bad62f2a tools: make_ext4fs: switch to LEDE git mirror
98b960c218 tools: make_ext4fs: support creating empty filesystem images
7347c14cd7 mvebu: rework ClearFog bundle.tar.gz generation
5b1c00e4fa bcm53xx: support USB 2.0 controller on BCM53573
62c5f68095 bcm53xx: backport USB 3.0 controller init patch
e674c1aab3 bcm53xx: backport USB 3.0 Northstar PHY driver
b9d8c81018 bcm53xx: rename PHY patches to use 07* prefix
b9b665ae49 mvebu: add ClearFog .tar.gz bundle
3c2c31bb66 kernel: backport upstream challenge ACK fix (CVE-2016-5696)
cf8da98e94 brcm63xx: switch to board based failsafe networking
6c9588ddf5 base-files: configure switch in failsafe
072cf26729 base-files: allow failsafe to configure vlans
c18edcec45 base-files: add preinit ifname detection based on board.json
0f1ae840c9 base-files: split out preinit interface config
780ccbf9f1 base-files: board_detect: allow specifying the generated file
e934a129f0 base-files: let config_generate call board_detect
0ddae04c22 brcm63xx: backport mtd of node changes from upstream
86ec410418 kernel: check SOURCE_DATE_EPOCH before setting KBUILD_BUILD_TIMESTAMP
5fe923b15d kernel: allow reproducable builds
4e8c6f3407 dropbear: security update to 2016.74
f76f83de71 mwlwifi: upgrade to 10.3.0.18-20160804
08a27b99a2 kernel: add missing config symbol
a9b1a429ab oxnas: set preinit network interface
592c0a1cd2 ramips: fix legacy image build
9d56ec6244 kernel: fix crashlog issues on highmem systems
fa350d5aba bcm53xx: add profiles for Buffalo devices
b835d7e811 bcm53xx: include USB modules in images for devices with USB ports
0b9de8daa7 bcm53xx: add profiles for all other (SoftMAC) devices
4d39726b21 ath10k-firmware: Update to latest 99X0 CT firmware.
f85c12e07d ath10k-ct: Fix loading 9980 firmware.
5d0b180f79 tools: flock: add NFSv4 compatibility
360fd10ac9 gcc: optionally build gccgo compiler
1645abffea kernel: add plan 9 fs package
dff6df9625 hostapd: Allow RADIUS accounting without 802.1x
eae422eb94 lantiq: fix some ethernet driver SMP issues
d378a7c4f7 bcm53xx: convert (disabled) Netgear R8500 image to own profile
931d309203 bcm53xx: add profile with brcmfmac for Netgear R7900
c769c1b584 bcm53xx: add profiles for devices with FullMAC chipsets
0f73801f4f ramips: Add support for Thunder Timecloud
5fadd4397b preinit: use only the image config options
14e0f057c8 ltq-hcd: fix xway dependency
7f22580078 kernel: adm6996: set carrier status
2b1f4945b1 ramips: Add support for TEW-714TRU
5947f7f85e lantiq: enable cpu temp driver for selected boards
0b327c1652 lantiq: board.d: set lan mac address only where necessary
47d3909415 lantiq: drop duplicate and now unused "lantiq, eth-mac" binding
91d5067091 lantiq: use the etop driver DT bindings only
1b7d6583a5 lantiq: fix mac address increments
a7cce111db lantiq: drop orphaned eeprom-handling code branches
12fe4b5798 lantiq: use ath, eep-flash/mac-offset for ath eep nodes
21f460a5db ath25: fix duplicate LZMA compression
7ee9222770 openssl: re-enable CMAC support
27dffa0b0c uclient: change SSL support error message
bebcb81da5 ramips: switch from 24kec to 24kc
b34ccf45df mac80211: Update the regdb to master-2016-06-10
22ef1c83b3 kernel: make the kernel build auto-clean the build dir like package builds
51e70267bd hostapd: remove unused hostapd-common-old package
ac642a7514 ath9k: improve powersave filter handling
4701fd3190 ath9k: improve performance in tx status handling
1b9dbb8532 Revert "kernel: remove long obsolete gpio spi controller driver patch"
6175115541 ar71xx: add missing LZO support select for routerboard devices
002b453687 kernel: add -mtune=34kc to MIPS CFLAGS when building for mips32r2
ecf7671b76 gcc: add a patch to generate better code with Os on mips
7c874d18f5 kernel: mark compression modules as hiddden to obsolete the compressor kconfig hack
93fb6ce05b kernel: mark kmod-udptunnel as hiddden to replace the NET_UDP_TUNNEL kconfig hack
577f873daf kernel: remove unused morse led trigger driver
9e62a7668c kernel: remove long obsolete gpio spi controller driver patch
99dd163bc3 kernel: remove a long obsolete unlzo decompressor fix
08fe1c6dbc kernel: remove obsolete slab tuning patch
56cf1adc50 kernel: remove esfq qdisc
3004298e62 sysupgrade: unmount filesystems before reboot
188517144e tools: lzma: reduce copyright noise
877168993a base-files: remove dead code
2180b715c1 image: fix per-device rootfs build error when not all opkg package files are found
9bfa6971ae scripts/config: properly handle select on symbols with unmet direct dependencies
2d7e602381 scripts/config: sync with latest linux upstream
7bf3695b02 kernel: clean up 260-crypto_test_dependencies.patch to get rid of some more kernel bloat
fa85ee1d4e kernel: modularize bridge netfilter support a bit further to get rid of some kernel bloat
a5c32a1f19 kernel: remove switch driver kmod packages
281483e097 ramips: enable nand support for mt7621
4df2011794 include/image.mk: allow image code to override uImage name
8e75630d1d ramips: updated remaining profiles to the new image building code
d3b21bb2bb x86: enable CPU frequency scaling
6e68a5dd11 linux/modules: Add SCH5627 Super I/O chips
828e25e325 lantiq: add cpu temperatur sensor driver for xrx200
2feb9433e2 rtc-rv5c386a: package does not build inside the SDK
10f9ea0bc6 uboot-lantiq: package does not build inside the SDK
9abbaa9539 build: remove MIPS dsp/dsp2 CPU_SUBTYPE
f2de33b2c9 build: move merged package directory from bin/ to staging_dir
2f8c355850 mkelfimage: remove package, it is a host tool that has been unused for years
fb35ac857f ar71xx: remove useless minimal/ath5k profiles
cc7029f8a9 uboot-ar71xx: fix default selection for NBG460N/550N/550NH
0cd13c53c1 mac80211: fix minor memleak on AP restart / warning on driver unload
18373e24cf ath9k: fix sta initialization bug leading to stability issues
349a3a127c omap: remove CONFIG_SND_DEBUG override
0a9fdeca6e kernel: add missing config symbol
1e0f650d7d feeds: switch from github to lede-project.org mirrors
2694d43b05 gdb: fix build with gcc 4.1.2 as host compiler
34bffe5806 scripts: fix remote-gdb with CONFIG_BUILD_SUFFIX
941ebafda0 lantiq: enable missing ath10k firmware for BT Home Hub 5A
83175687c8 build: remove image specific checksum code
27854a0a84 build: add checksum target
4d9fc1bd44 apm821xx: fix IB image building
5c9cc7b7f8 base-files: increase vm.min_free_kbytes
df3a2ca1a9 kernel: re-enable CONFIG_SND_VERBOSE_PROCFS (FS#66)
1bcad76395 ar71xx: Make wget2nand look for LEDE project firmware files
f3fbc80718 ipq806x: fix MAC_POWER_SEL for Netgear R7800
109c55aea1 uqmi: add metric option to interface config
15867deac8 uqmi: fix option ipv6
686617ae39 ramips: Rename TP-Link Archer C50 LEDs
dbf107cd2b ramips: Improve TP-Link Archer C20i support
d4abe72cce target/sdk: update README.SDK to explain dependency handling
847cb10f47 target/sdk: ship toolchain and kernel module package
905e50d2fb image: use the merged package directory to resolve dependencies for per-device rootfs
180465c38f build: create a package feed directory containing all packages
e351f7c695 build: fix tabs vs whitespace issue
4ab33a3002 brcm63xx: fix CT-536p/CT-5621T support
ea6a3be62e kernel: silence a false positive uninitialized variable warning
532eb5f581 ipq806x: fix boot hang if cmdline contains words with r in the middle
ba1aa4e33b mvebu: fix NAND flash issues (FS#67)
5d9a4c210d imx6: clean up / fix ventana image build code
94dec60d75 build: add template for installing device .dtb files
468a9b7a77 imx6: use ubinize-image.sh to fix build with per-device rootfs
1448501558 build: do not depend on svn any more
df68d6eb15 brcm63xx: fix build with per-device rootfs
62d4665551 ipq806x: add missing sysupgrade-nand => sysupgrade-tar change
14488469d5 image: fix build issue with per-device rootfs and legacy devices
5e41c1d447 perf: prevent build from within the sdk and mark as nonshared
12703d5b29 sdk: provide a config symbol for detecting builds within the SDK
63b525dd6b image: add a helper variable for getting kernel/rootfs from within image Build/* templates
9201e88f51 kernel: remove hostap driver
467dee32ed octeon: increase block2mtd rootfs probe timeout on ER
baeda5d31d image.mk: add CMDLINE to DEVICE_VARS
67e764c6ca octeon: pad squashfs sysupgrade image rootfs
84718d8736 image: add support for overriding kernel/rootfs images in sysupgrade-tar template
77b16bacb1 octeon: drop unsupported jffs2 feature flag
2192a029d3 octeon: fix sysupgrade images
9a3852bf8c kernel: fix crashlog regression on x86
50e7c1f79d include/cmake.mk: fix host builds
b2ddfbc1c7 dnsmasq: drop --interface and --except-interface options when the interface cannot be found
eadf5fb7f8 cmake: include/cmake.mk add CMAKE_BINARY_SUBDIR to allow out of source tree builds
009d6d6024 netifd: update to the latest version, adds an event handling fix
5cd88f4812 dnsmasq: remove use of uci state for getting network ifname
c5a9a08f1e image.mk: remove leftover variable from a previous rework
18c622a1f2 ath25: rework image building
db49dd894e build: rename sysupgrade-nand to sysupgrade-tar
fccc4298df octeon: clean up image build code
a1681ce39b dnsmasq: replace the iface hotplug script with a procd trigger
6916ca8d33 dnsmasq: make the check for existing DHCP servers more reliable
712b6fdc5c dnsmasq: write atomic config file
d9ff187003 netifd: update to the latest version
f88e3a4c0a procd: add default timeout for reload trigger actions
c02f41c1d2 igmpproxy: remove procd_open_trigger/procd_close_trigger calls
8299737428 dropbear: remove procd_open_trigger/procd_close_trigger calls
88304ea6e5 sysntpd: remove procd_open_trigger/procd_close_trigger calls
8891d941e0 procd: rework trigger handling
eed30bc869 procd: update to the latest version
11d47e615b libubox: update to the latest version, adds a few utility functions
f4ce133ccf build: add option to enable all profiles
76341cfc5f build: add support for per-device rootfs based on device profile packges
c0dceae4bb build: minor cleanup of redundant code
653cb2594d build: set TMPDIR for opkg calls
c792c7512c build: add target_params variable for getting root filesystem image parameters
731b166528 build: add template for getting opkg package files from package names
5d30bf8303 build: rework opkg command invocation
37e82e4e42 build: remove obsolete variables from opkg command
7dffc32ffa build: rework prepare_rootfs to pass target dir via parameter
c5ca181d12 image: add wrapper variable to get the target dir for mkfs commands
4fed7a60f9 image: make mkfs template output to $@
973e6e1d71 build: move rootfs processing code to include/rootfs.mk so it can be reused later
119b4422f8 apm821xx: only attempt to mount /boot on MyBook Live
47cce1d5e4 lantiq: fix switch configuration for EASY80920
6b5a418512 kernel: fix crashlog issues on various architectures
eb28a0cde6 lantiq: fix WBMR-300HPD switch port assignment
3bb2b46bc3 octeon: fix image build
adbbfb7ff9 ar71xx: don't use D-Link DIR-505 status LED as ethernet indicator
500a67a167 ar71xx: add revision detection for D-Link DIR-505 A1/A2
c58ed54d8c brcmfmac43430-firmware: update to v7.45.41.26
f6a86ba066 bcm53xx: enable kernel symbols/drivers needed for BCM53573
2552e9319e bcm53xx: backport DTS patches for USB 2.0 and Tenda AC9
a3be48593b bcm53xx: refresh kernel patches
96fa9aa13b ar71xx: add a missing ;; to ar71xx.sh
4a0c4d8151 netifd: Use -x hostname:$hostname instead of -H
e1406cd31a base-files: sysupgrade: fix pseudobridge upgrades
846eca673f b53: allow ports with higher numbers than CPU port
cea917c30b brcm63xx: fix HG556a C button
30d35181cd mountd: update to latest git HEAD
74766f4c4f firewall3: update to latest git HEAD
b15f41d4d6 ugps: update to latest git HEAD
525b9edc8a ramips: unify etc/board.d/01_leds configuration
42305ae24a ar71xx: add support for gl-mifi
0d5277f73f ramips: dch-m225 don't have ethernet. default enable wifi
104114fe00 ramips: remove indentation in etc/board.d/01_leds
6674006bd0 ramips: add missing i2s alias
9687341808 ar71xx: clean up legacy-devices.mk
7cc31b52e1 toolchain/gcc/arc-2016.03: Fix building on hosts with gcc 6.x
da328f2865 hostapd: backport mesh/ibss HT20/HT40 related fix
86c0a569f4 fstools: update to latest HEAD
35e423ca41 base-files: use procd init for urandom_seed
b8cd996d92 mvebu: limit image builds to profile selection
5fd2eabeb2 base-files: remove support of profile-specific base-files
776ca66261 ath9k: fix warning in client mode (GH#195)
b47f438d98 build: remove image prefix from kernel files in KDIR
9945a1dca5 build: remove cpio.gz and tar.gz from regular filesystem types
33c8d35375 image: remove shell calls from legacy ubi/ubifs image code
064bcdc259 kirkwood: fix UBIFS_OPTS variable in image build
d0619fb02c Remove existing old link before creating a new one
3f506bdbb0 apm821xx: fix atheros PCIe cards on the MR24
08257a4053 apm821xx: use lzma compression for the initramfs images
04a6984319 ath9k: remove intermediate queueing patch until it is fixed properly
bafeb90745 iperf3: update to version 3.1.3
9cbb51ff8c iperf: update to version 2.0.9
bdf9243c1b cyassl: update to wolfssl version 3.9.6
7d38128f6a curl: update to version 7.50.0
cd91f384ac openssl: re-enable NPN by default
cb8f322d93 openssl: add back the CAST cipher by default
07577c5ebe tools: bring back genext2fs for apm821xx
18f368fa35 linux: Get rid of 000-keep_initrafs_the_default.patch
600fd467d8 openssl: revert the no-ripemd change, openssh needs that cipher
164a405a48 ath10k: Support installing CT firmware for QCA9984 NICs.
9971ab0457 ath10k-ct-firmware: Update to latest 9880 firmware.
eb8ffbebf8 ath10k-ct: Update to latest ath10k-ct driver.
84a1a0edf0 sunxi/pcduino3: Remove selection of absent rtl8188eu
3ad8bc4366 openssl: add option to disable SRP support
057b116e09 openssl: add --gc-sections
41da31ac2c openssl: remove some unneeded functionality and algorithms
f16fc21675 openssl: add option to disable PSK support
0099748fd6 openssl: add option for NPN support
eb4fc91a81 openssl: add option to disable compression support
db11695aa6 openssl: add option to omit deprecated APIs
8fb89f7e73 ledtrig-usbdev: fix duplicate match detection
f1e085adfe ar71xx: add ath10k firmware to profile defaults where ath10k is used
11fc0cd1b1 image.mk: create default ubifs before calling legacy image build code
39429b3d20 apm821xx: rework image build code for MyBook Live
3886644632 apm821xx: add DEVICE_DTS_DIR variable, remove redundant DEVICE_VARS entry
44c39d5812 apm821xx: add missing default profiles for subtargets
9e0fd1b52a apm821xx: add support for the Netgear Centria N900 WNDR4700/WNDR4720
47eeb9f857 apm821xx: lm90 add thermal sensor interface support for device tree
b46e2a6d95 apm821xx: tc654: add driver for Microchip TC654/TC655 PWM fan controllers
dc7efaefb5 apm821xx: add support for the Western Digital MyBook Live Series
d37d16488c apm821xx: sata_dwc_460ex: backport fixes and cleanups from 4.7
ea91ee13a7 apm821xx: dw_dmac: backport fixes and cleanups from 4.7
a57d6e2d47 apm821xx: add support for the Cisco Meraki MR24
3827ce2c3d apm821xx: add support for the apm821xx device target
39f3408732 ppc4xx: remove booke-wdt watchdog package
e6a7e6ed25 lantiq: fix image creation of P2812HNUF3 & BTHOMEHUBV3A
b82c8ddf8c libpcap: fix dependency of install-shared-so make target
c7a5bb5a7e samba36: avoid picking up a dependency on libunwind (fixes GH #212)
ca6375ac51 hostapd: fix an error on parsing radius_das_client
14eb09d5c0 ath10k: add NAPI support
467d15b73d mac80211: add a mesh related fix
d22fc1973c kernel: enable CONFIG_SND_PROC_FS by default (FS#54)
ab3bf82e01 toolchain/gcc: disable libmpx to fix build errors on x86 with gcc 6.1
c6c81351b7 ar71xx: add missing profile for the nand subtarget (FS#56)
16209710d9 ar71xx: fix WNDR4300v1 / WNDR3700v4 build (FS#56)
ad323881df ar71xx: fix more image build code whitespace/tab issues
8265fdcc4d imagebuilder: strip DEVICE_ prefix from profiles (FS#55)
ed90d50bc4 build: fix image builder profile override (FS#55)
3d8c8d5e05 ar71xx: fix tab vs whitespace issue in image building code
4d0f4f5e52 ar71xx: remove obsolete MultiProfile template code
32727c409e mvebu: switch to the new image build code
60d2620253 kernel: update bcma backporting changes up to 4.8
d12e276cb0 kernel: backport patch for MTD_BCM47XXSFLASH dependency
7a175e2d44 ipq806x: clean up redundant initialization of core device image variables
b5b2425cba image.mk: initialize BOARD_NAME and IMAGES, add it to DEVICE_VARS
9a50a213d2 image.mk: add support for specifying the VID header offset for UBI
cd243b1090 cns3xxx: remove obsolete jffs2 image build code
eceb6b924a x86: remove obsolete reference to $(PROFILE)
673004f9bc config: remove options for including kernel/dtb in rootfs
2b4d21a3e6 mxs: unconditionally install kernel images/dtb files into rootfs (needed by boards)
650afe412b kirkwood: remove obsolete code for including kernel/dtb in rootfs
edea59fd99 omap: remove obsolete code for including kernel/dtb in rootfs
1625e57772 omap: remove obsolete kernel version support
0538bbdc4d kirkwood: remove obsolete ubinize.cfg file
5d4b044955 kirkwood: clean up redundant variables in the image building code
cfd1ef4b90 kirkwood: get rid of useless ubifs/ubi option variables
ab92f57684 lantiq: convert remaining xway NAND devices to new image build code
f12e964733 lantiq: convert AVM xrx200 devices to new image build code
bdfed2a2c3 lantiq: convert simple xrx200 devices to new image build code
22c0206044 lantiq: add image build template for NAND devices
8058e4778b lantiq: simplify image building code
cc88df1a38 lantiq: fix building NAND images in default config
9497a23ecb build: add support for parameter passing to mkfs from devices
4added6692 build: split legacy image mkfs.ubifs command from the one used for the new image building code
ebd0b2d0b1 build: split legacy image building code out of image.mk
d7b185128d build: make TARGET_ROOTFS_JFFS2 depend on USES_JFFS2
ceee47ba64 lantiq: disable jffs2 support on xrx200
1c1244193a image.mk: replace some template abstraction with make pattern rules
efdf7f6499 image.mk: remove obsolete Build/mkfs overrides
5a92e049d5 kernel: remove obsolete patch adding usb_find_device_by_name
5ea8756766 ledtrig-usbdev: use upstream function for iterating USB devices
e633a1b48f ar71xx: fix default network config of WZR-HP-G300NH and CR3000
d963ddf042 ar71xx: add support for gl-ar300m
6c2651566c ath9k: switch to using mac80211 intermediate software queues
4221288db7 x86/generic: enable CONFIG_SATA_VIA
122a7021a9 ubox: update to the latest version, fixes lsmod output
6b654ab741 uboot-oxnas: fix build error on non-linux systems
022698c6c9 kernel: backport cosmetic UBIFS patches to kernel 4.1
fc90851df0 kernel: backport yet another cosmetic ubifs patch
9b05d3aa8e strace: update to version 1.12
f082d94235 oxnas: add kmod-ledtrig-timer to default package set
8880497382 oxnas: use DHCP by default on ethernet interface (lan)
b05125c775 oxnas: sync kernel config-4.1 with changes made to config-4.4
caf36d199d oxnas: add DTB for Akitio devices in patches-4.1
c5ec5e1f7f oxnas: revert to kernel 4.1
56f686b710 samba36: disable local browse master by default
75329fc161 hostapd: fix VLAN support in full wpad builds
9780b2dd93 ipq806x: add patch for kernel compiler flags
15bcda4be6 ipq806x: change compiler flags to arm cortex-a15
4e5a8c4c6d feeds.conf: disable the targets feed by default
7cdb51e046 ath10k: fix stack traces from a-msdu rx reporting issues
efdd3bf5fb scripts/getver.sh: fix older git versions from printing stuff to stdout
b051ac76e8 ramips: mt7621: add missing kernel symbol
900da27c91 ar71xx: add software transmit timestamp support
207338c78e ath9k: implement temperature compensation support for AR93xx and newer
98e4b504b4 ath9k: use external reset on AR91xx and QCA955x to improve stability
a176168a85 ar71xx: define wmac reset function for QCA955x
7bdc21de72 image.mk: fix append-dtb race when multiple devices use the same .dts
b948c9371b uclibc++: fix build with gcc 6.1.0, which defaults to using C++14 ABI
445604a915 toolchain/gcc: add 6.1.0
a4e90e2cac toolchain: get rid of GCC_VERSION_5 config symbol
e031940570 toolchain/gcc: clean up remaining references to the old linaro version
d4916359c0 toolchain/gdb: update to version 7.11.1
0aa6450840 toolchain/gdb: reorganize patch layout
0f4a337b31 toolchain/binutils: add 2.26.1
dc8da205cb tools/isl: bump to 0.17.1
3273267c2b ath9k: fix spectral scan on AR9285 and newer AR92xx chipsets
9edb651094 ath9k: merge a fix for the minimum CCA threshold on 5 GHz
f021ea47d3 target.mk: change CPU_CFLAGS to better suit target CPUs
11d496d156 target.mk: rework arm architecture level detection
8e2764ce9b image.mk: clean up redundant code related to DEVICE_DTS
7ed215437c scripts/getver.sh: stop relying on the reboot tag
55761205ef mac80211: fix a harmless uninitialized variable warning
1c52826010 add ath10k-ct: Candela-Tech ath10k out-of-tree driver.
c940ccedd8 bcm53xx: image: don't suppress "mv" command echoing
b3b797076e bcm53xx: simplify image building code
dbc416b6ec bcm53xx: remove duplicate template data from the image makefile
b8fddb8912 image: allow devices to override the -E 5 ubinize option
e0ed6ec667 image: clean up UBI related device variable definitions
1729a089fe ipq806x: remove obsolete UBINIZE_OPTS variables
d43075710b mbedtls: fix missing mbedtls_time_t bug in mbedtls 2.3.0
3e5b50a8a7 musl: remove sh3 workaround
9816d2f5f5 musl: update musl to version 1.1.15
2d3917d5b5 gcc: update gcc to version 5.4.0
05cc72944c mbedtls: update to version 2.3.0
bd20cb272e polarssl: update to version 1.3.17
57530dbec6 dosfstools: fix build on OS X
14ee2b0642 uboot-envtools: add support for jjPlus JWAP230
d2c9b169b3 ar71xx: add support for jjPlus JWAP230
2923b334e5 kernel/mtd: add support for EON EN25Q128
c30fd5e87d uboot-envtools: add support for Wallys DR531
e767980eb8 ar71xx: add support for Wallys DR531
3c6b091b65 sdk: Allow to configure signed pacakge lists
70cf8c3048 ar71xx: fix build error when initramfs is disabled
6f86d2e2ab scripts/getver.sh: fix one more wc -l call
4eb5aad667 scripts/getver.sh: try to get branch/upstream automatically
efa1960abb kernel: update kernel 4.4 to version 4.4.15
d6b3b44d97 ar71xx: fix a legacy image porting issue
2ea76bdf04 x64: add legacy IDE, fix VirtualBox bug #84 and Fujitsu Futro S550-2
4952469ff9 mac80211: disable fq until performance issues have been found and fixed
99e5bec2c6 netifd: quote vendorid and hostname variables in dhcp script
cef1f4ef2b ath9k: explicitly clear gpio chip owner
5b07e8731b ath9k: remove gpio chip owner field to fix module unloading
5ce2341a03 mac80211: fix a powersave issue in the intermediate queueing code
4f106d6c07 Revert "ath9k: switch to using mac80211 intermediate software queues"
4ebb1950be kernel: Add upstream fix for module loading
697ee80388 Revert "linux: arc: disable kernel unwinding to fix modules loading"
055ba75f92 linux/archs38: Add wireless AP capabilities similarly to axs101
9352603fff mtd-utils: merge ubi/nand-utils into one package
17f4d3967e samba: update smb template socket options defaults
3dded42f05 iftop: fix mac address display
ef3c0cf590 procd: update to latest git HEAD
527696674a igmpproxy: logging options - make work & improve
a775c5db46 ar71xx: Fix PowerCloud CAP324 No Cloud title
9062c4fe99 ramips: modify audio kernel module and add dma options
c3e420f28c ramips: Add support for D-Link DCH-M225
36d98e6c7a ramips: add MT7620 pinmux bits for mdio as refclk
0460e9ffca ramips: enable MTD_SPLIT_SEAMA_FW for mt7620
cf8c77be6b ramips: Add support for the NixCore X1 Module
8876575601 ramips: fix partition size for RT5350F-OLINUXINO
252f751611 ramips: fix usb phy initialisation
09907170dd ar71xx: base-files: remove the now unneeded 09_fix-seama-header
8d0ec3e672 ar71xx: image: fix typo in MTDPARTS def for qihoo-c301
6d6db4ff7b ar71xx: image: seama: fix making factory and sysupgrade image
d06b68fe83 tools: padjffs2: add option to output padding data to stdout
31e5ed4152 ath9k: switch to using mac80211 intermediate software queues
c19381dfca scripts/getver.sh: fix revision number on BSD/MacOS
916aebb300 ath10k: fix a compiler warning
73dd59546b ath10k: fix #if vs #ifdef in led trigger patch
78ae53ff2f mac80211: make package ath9k-common hidden
f4293e476d brcm2708-gpu-fw: update to latest version
20402106a3 brcm2708: update linux 4.4 patches to latest version
f1765277ba scripts/getver.sh: avoid use of git rev-list --count
eae812ddb6 brcm63xx: fix image generation with offsets/blocksizes != 64K
0bed85bbca brcm63xx: fix CVG834G compatible string
15b88df87f scripts/getver.sh: improve revision output
1001b5d77c scripts/getver.sh: allow conversion between git hash and revision
575be9d182 scripts/getver.sh: simplify revision calculation
c729fe0269 mac80211: backport brcmfmac changes from 2016-07-08
fac693441f bcm53xx: fix kernel config after USB2 PHY driver backport
d98409edbc mt76: update to the latest version, fixes powersave issues
74c9b9cfeb toolchain: skip gcc/minimal for musl
1692c71564 bcm53xx: use upstream fix simplifying USB power GPIO usage
c74c227e5b bcm53xx: backport driver for Northstar's USB 2.0 PHY
e71fffed64 bcm53xx: backport BCM5301x patches from 2016-07-06
d8dbd33eba scripts/package-metadata.pl: fix kmod pakage dependencies within the SDK
b80dfe4cde scripts/diffconfig.sh: fix handing of CONFIG_TARGET_MULTI_PROFILE
07e8cfed8a mwlwifi: Update to latest version
2f2d1829be target.mk: fix ARM architecture feature flag detection
bcb1d9399f valgrind: update to the latest version, fix build issues on ARM
01fc738b46 tools: build b43 tools if the SDK was enabled
c1c49d9456 prism54-firmware: change prism54/p54-firmware package versioning
1b13b35231 include/toplevel.mk: fix defconfig when ~/.openwrt/defconfig exists - take 2
8d95b665e8 mac80211: backport brcmfmac changes from 2016-06-29
201dbb9fe8 ramips: fix build error in ubnt-erx initramfs factory image
ad430c1080 hostapd: add a WDS AP fix for reconnecting clients
5b72807416 include/toplevel.mk: fix defconfig when ~/.openwrt/defconfig exists
aba6de38d2 usb: Remove annoying warning about bogus URB
2005732ea7 linux/archs38: Disable USB 2.0
1cc092f72b lantiq: mac address setting on BTHOMEHUBV3A
17ee6bb8f3 tools: add kernel2minor utility for Mikrotik devices
a3e7d5e7ae samba: Update smb.conf.template
b9952797e6 kernel: Move POSIX ACL and attr support options into submenu
eca1021e5c ramips: fix buffalo wmr-300 lan port
8fe69e4d42 ar71xx: fix nand device profile
9a4345069f procd: update to latest git HEAD
21fa645f7a uci: update to latest git HEAD
cbf6bc296f usign: update to latest git HEAD
d643ee0260 umbim: update to latest git HEAD
1a06dc6dc2 libubox: update to latest git HEAD
2c9073282d ramips: fix MT7621 gsw handling
69a626b441 ramips: fix mt7621 SoC detection
34527688fc scripts/feeds: Prevent .config autocreation
a7f6dc9f8b px5g: Create mbedtls variant
df2889c709 packages: fix bmp085-spi typo
bd7289af38 uclient: update to the latest version, fixes HTTP redirect support
92d856f50a ath9k: add beacon related stability fixes
71753a8286 Revert "ustream-ssl: Fix recursive dependency"
dd9afb8207 iwinfo: fix nl80211 phy lookup without platform prefix
70b4e46804 e2fsprogs: fix build on OS X systems
eaf0d22421 bcm53xx: calculate Seama MD5 using content of kernel partition
3c014dc306 Revert "bcm53xx: use uncompressed zImages"
a1b52e2b53 dosfstools: update to v4.0
39a229ed4b ipq806x: enable ath10k firmware for 988x, 99x0 and 9984 by default
abf0768131 ustream-ssl: Fix recursive dependency
d09f0045ea ramips: fix up switch settings for Sitecom WL-351 v1 002
e892472b1e x86: enable kmod-igb on 64-bit by default
f5088dc13f kernel: fix duplicate drivers for the PC speaker in one package
d5ee23ee27 x86: stop relying on hexdump for image build signature
f226d5879e mac80211: move include statements for skb_get_hash_perturb() to prevent issues with newer kernels
b174832159 mac80211: backport skb_get_hash_perturb() for 4.1 and older
70afc0bdd1 kernel: mac80211: set the parent of the ath9k gpio_chip
7b7ea91e24 kernel: mac80211: enable the gpio controller for all ath9k devices
3ce71eaedd kernel: mac80211: fold the AR9280 GPIO patch into the ath9k GPIO patch
cbfeb7796e mac80211: refresh patches
76d09dcb01 ath10k: fix tx performance regression on older chipsets
d002aee42c mac80211: enable STBC and LDPC for VHT rates
898fff8253 ath10k-firmware: add symlink for QCA9984 board.bin
67a7daa938 mac80211: update to wireless-testing 2016-06-20
de165b66be imx6: fix redundant PROFILES overrides in image makefile
7e7a31e682 imx6: fix build breakage introduced in 9e41c3f54e3c
61d82e7b02 imx6: fix image makefile indentation for Device/ sections
1d15a96b29 kernel: fix build of kmod-udptunnel4 and kmod-udptunnel6
2a8bb46294 jsonfilter: update to latest git HEAD
8a83ffbefd procd: Set /dev/kmsg to 600
bb00c0a33c fstools: update to latest git HEAD
a74f593647 procd: update to latest git HEAD
c5a2713929 ubox: update to latest git HEAD
1e9c066595 ustream-ssl: update to latest git HEAD
25275bcc24 ubus: update to latest git HEAD
c312cef223 ar71xx: spi-rb4xx fix.
3fbadd624a nand-utile: add package
f9e7ffe73b ar71xx: prevent spurious ethernet resets from dma hang check false positives
f28502a485 libnl-tiny: Generic Netlink multicast groups support
f576ff05a1 kernel: Fix ipv6 mc snooping if bridge has no ipv6 address
97c90557a9 spidev_test: copy the source code into the package folder
66b67b743f kernel: other.mk: add pps-ldisc support
559a7d1177 ar71xx: seama: fix making factory images
ea284d704b ar71xx: image: unify indentation with 2 whitespaces
e3cf2cc1c6 ar71xx: image: remove duplicate IMAGES definition
11cbe29833 ar71xx: hiwifi-hc6361: move packages selection to generic.mk
9597675d8e procd: change /dev/{gpio,hvc*} perms to 0600
c6cef6dde7 procd: adjust /dev entries to desktop distro defaults
2dc9beddc0 ramips: disable the WP pin on the SDK mmc driver
81add8f753 ramips: fix pinmux typo
3946a55291 base-files: seed /dev/urandom
e408abd7fb kernel: Add option to make using filesystem ACL support the default
3ee278c5c9 package/kernel: Enable XATTR by default
d635ef50c5 e2fsprogs: fix build problem with very old libmagic
ffcae8b494 prism54-firmware: add also other p54 firmware to own package
37fa64a6c5 firmware: extract prism54-firmware into own package
0a0caa2656 ramips: set correct LAN/WAN MAC addresses on DIR-860L B1
103ed00cfb ramips: add button support and make LEDs known to userspace for DIR-860L B1
fa9811814a ramips: fix fixseama call on first boot
ecbc138343 odhcp6c: Upstep to latest version
0b208a7de1 kmod-sched-cake: Switch to COBALT algorithm
6d7f54ccdb iproute2: cake AQM prepare tc for COBALT algorithm
c2bd469521 dnsmasq: Add broken realtime clock build switch in full variant
95d9330d57 rpcd: iwinfo plugin fixes
19aae09f5f kmod-bmp085: add dependency on !LINUX_3_18 !LINUX_4_1
93d5629a27 modules: add BMP085 pressure sensor
1e03998e2b mac80211: fix skb size calculation in 4addr mode (FS#24)
8d51706616 base-files: use LEDE NTP vendor pool
f98f4601de openvpn: fix missing cipher list for polarssl in v2.3.11
4a3b8e0596 lldpd: Use /etc/os-release instead of /etc/openwrt_*
6ee66ae075 ar71xx: further legacy image build fixes
2270fc5947 Revert "lantiq: enable SMP for XRX200"
be08fdd007 ar71xx: disable pdata->use_flow_control for QCA9558
75b2105cd3 ar71xx: rename ethernet pdata->builtin_switch to use_flow_control
8d1218ca73 ar71xx: merge profiles into image building code
dc140e00a9 kernel: fix missing break in ubi auto-mounting patch
459a8afff1 kernel: remove igb: Fix Null-pointer dereference patch
bf32177a1d kernel: remove full cache flush in fuse_copy_do() for MIPS
2abb02419d kernel: remove one of two patches deactivating broken vdso support on mips
84d489f64f kernel: update to version 4.4.14
3bf3512673 Revert "ar71xx: prevent spurious ethernet resets from dma hang check false positives"
86a2702a00 libnetfilter_queue: fix checksum computation
e6b9330343 build: Adds the ability to disable personal initramfs build for target device
3d58d7f053 ar71xx: prevent spurious ethernet resets from dma hang check false positives
26b8db2537 ar71xx: enable flow control for ethernet MACs with built-in switch
9493613e94 linux-firmware: fix md5sum
2ca4fa5feb rtl8192su-firmware: move firmware to own package
d2a372c4fc rtl8192se-firmware: fix package build
3874773503 Revert "ar71xx: fix legacy image building"
cb7aa4b1fe ebtables: fix segmentation fault due to uninitialized extension data
d4ede1c118 base-files: sysfixtime no longer exclude dnsmasq.time
5acfe55d71 dnsmasq: dnssec time handling uses ntpd hotplug
f954f4337b base-files: Add standard os-release file
59e98b27c9 ar71xx: fix legacy image building
819cf75c40 tools: e2fsprogs: bump to 1.43.1
636089ead6 ar71xx: merge profiles into image building code
5fba0f0c0c ramips: add suport for ZBT APE522II
27493e82f9 mountd: update to latest git HEAD
184087f4f1 ipq806x: enable ieee80211 phy hotplug and patch macaddress
f97ad870e1 squashfs4: use upstream xz compression header format
f080cfab72 lantiq: fix network in failsafe
acd41539d6 linux: arc: disable kernel unwinding to fix modules loading
776613eeba ipq806x: Fix typo in Qualcomm device names
3f38356893 packages: prefer http over git for git protocol
b32eb40210 uboot-lantiq: Add Arcadyan ARV7506PW11 support
9759fde40a lantiq: add support for ARV7506PW11 (Alice/O2 IAD 4421)
b67066b8fa ar71xx: hiwifi-hc6361: lift size limit on kernel and rootfs parts
b7baaaf782 kernel: Move append-dtb to common image-commands
7385f754b1 lantiq: Correct ADSL race condition
34fdfbf328 lantiq: Slow down SPI flash on the DGN3500
f054e82bdc lantiq: remove gr7000 support
823242185b ipq806x: add initial support for Netgear R7800
9bf3ddcb2a ipq806x: move ath10k firmware selection into device profiles
4cd67a4f21 ipq806x: move smb208 nodes into a regulator subnode
84b3d92180 lantiq: make EASY80920 work with both chip versions
7f5b8cc376 lantiq: use new partition layout for EASY80920NAND
8bfa230e9f lantiq: build fullimage.img for EASY80920NAND
ecdfbeae85 lantiq: remove patch adding support for building without reset controller
ee613097be tools: patch-image: Added optional size option
63cb2fb88d brcm2708: properly detect the Raspberry Pi Zero
a95d64a269 brcm63xx: simplify block size and image offset options
13253fbcbd brcm63xx: add sysupgrade images
7df43d88ec lantiq: fix typo in new image generation
040ebe2473 ath10k-ct: Update to latest 10.4.3 CT firmware for 9980 chipsets.
9da1bf58b6 sdk: Fix keeping unset as unset
5d60bedcb3 ath10k-firmware: fix board-2.bin download URL
d61d82e3d3 brcm63xx: merge DSL-274X-F1 profiles
a89f5e795a brcm63xx: move the bootargs into the dtb files
80403e4558 brcm63xx: use upstreamed compatible name for the periph intc
29444e4754 brcm63xx: fix external IRQs
6b5f6d6601 brcm63xx: fix single profile selection
a180f90518 bcm53xx: backport BCM5301X patches for SRAB
65a22d84ad kernel: backport bgmac changes from net-next
4bd0edba1e kernel: rename bgmac patches that went into the same kernel
163cc22643 procd: properly set /dev/snd permission and group
e2d2b136b3 e2fsprogs: Bump to v1.43.1
81913e4996 ramips: remove duplicate i2c dts info
60ccfbbad0 ramips: update i2c drivers
66ffd0ddf9 ipq806x: fix MAC_POWER_SEL switch configuration
153b3f05d4 lantiq: BTHOMEHUBV5A - use the power event code for the restart button
551c9c8300 lantiq: diag - switch off the power led on failsafe
32012decc3 lantiq: fix build of NAND sysupgrade images
ac1cc30cdf lantiq: ltq-atm: fix xrx200 depends
e4bad7953b fstools: fix missing dependency
776b24d9aa bcm53xx: properly support sysupgrade using Seama on NAND devices
7e08f2ccbd mtd: support -c (datasize) option for fixseama command
cf6d9d97fb kernel: rename B53 symbols to avoid upstream kernel conflict
1aca291214 kernel: mtdsplit: calculate kernel partition precisely for Seama
fac7ba1abc uboot-envtools: add support for ZBT-WG2626
67475b0e31 kernel: backport cosmetic ubifs patch
982108f7e5 lantiq: clean up / fix LegacyDevice template handling
f4c59a204e lantiq: get rid of ifneq() checks inside command templates
8a156ad129 image.mk: add a separate step for building kernel images for LegacyDevice support
425e2c1d96 image.mk: run LegacyDevice prepare once instead of once per filesystem
3004275c17 image.mk: fix make variable/command context leakage between LegacyDevice templates
9a0381f969 lantiq: small fix for legacy profile builds
ff4a804669 octeon: fix image build
240137a744 mt76: update to the latest version, fixes a SMPS handling issue
e81020c317 medaitek: convert the NAND target to UBI
16e04fd1b4 procd: update to latest git head
87eb8fad13 base-files: remove fstab symlink
bbbe9932e3 ar71xx: WDR4300: Fixed default VLAN order
b180f24a3b Revert "ramips: update i2c drivers"
0ddcbee261 ipq806x: activate ATAG DTB mangle and EA8500 rootblock in dts
f532191c1c cns3xxx: fix RX softIRQ loop
137b1ac5e8 netlogic: R.I.P
ea828eb3af mountd: update to latest git HEAD
a6f7536a73 lantiq: convert remaining legacy targets to the new image generation code
4bab4dee84 ath10k: merge some more pending upstream fixes
c2e0c41842 Revert "ar71xx/cpe510: use second wifi calibration table"
475e94b1d2 uhttpd: update to the latest version, adds some extensions to handler script support
952beca4aa uclient: update to the latest version with better help and DELETE
71d533eea9 package-ipkg: do not include feeds.mk at metadata dump time to speed up scanning
4b8ba2b4ce include/feeds.mk: allow installation from feed packages that are installed but no longer in feeds.conf
3ee6c17cd1 package-ipkg.mk: fix Provides for packages with multiple PROVIDES entries
4e0a533f60 hostapd: fix breakage with non-nl80211 drivers
96db107524 tools/cmake: fix parallel build with Make 4.2+
6fb212f293 build: don't add -j for parallel builds with Make 4.2+
e2a9c638e7 hostapd: fix compilation error in wext backend
df18b3756f scripts: feeds: fix version detection for Make >= 4.2.1
a285f1895b Revert "lantiq: Use correct macaddr generating logic for the DGN3500"
70bb22037a hostap-driver: mark as broken, it causes extra bloat in hostapd and is probably not used anymore
c2ec43733a mt76: update to latest version, adds survey support for mt76x2
ef74d5cbf8 hostapd: implement fallback for incomplete survey data
13b44abcff hostapd: update to version 2016-06-15
b67af71181 hostapd: Update to version 2016-05-05
a3cde627f8 libubox: update to the latest version, fixes an uloop signal handling race condition
9fc250a481 realview: sync kernel config file
8e70655f35 mt76: update to the latest version, fixes a monitor mode injection crash
3a75777e86 lantiq: refresh patches
ad76366d7d kernel: refresh patches
be74158102 kernel: replace SMP cacheflush fix with some patches from linux-mti.git
b3be33f135 bcm53xx: use uncompressed zImages
e6d3899ddc kernel: add support for uncompressed zImage on ARM
af1791964d kernel: add common config symbols
f27c70ff8c bcm53xx: refresh kernel config
14e2f4f6d1 ipq806x: add missing kernel config symbol
1830c31632 mvebu: Configure status LED for WRT1900ACS
24cd658a9d realview: bump to v4.4
f966ea2f49 firmware-utils: oseama: support extracting entity
f77a56d18a octeon: export the FILESYSTEMS variable during image generation
7992633e63 octeon: Ignore MEM boot param when too small
9361285a41 ipq806x: restore old stmmac dma patch which is still needed to fix data corruption
e13b6322cd Revert "ipq806x: add mangle bootargs options in config-4.4"
e030c31e35 octeon: convert to new image building code
bfcbca3e04 mediatek/ralink: fix boardnames
719fd09d91 tools: build msdostools for omap
93276a351c omap: remove NAMESPACES config symbols
0dbd0b9ecd omap: remove XFRM config symbols
abf23d70ac omap: remove config symbol W1
4ff529665f omap: remove config symbol NETFILTER
21738fe01e omap: remove BMP085 symbol
5a5934f0c2 tools/mkfwimage2: remove 256 length limit for partition images
9233db23f3 lantiq: the io space was still not big enough for UHCI
88019c6c77 lantiq: add ARV4525PW wifi led
90c48dd49d lantiq: fix VG3503J loader generation
d5666b98fa lantiq: fix fritz7320 wifi support
98d00c35e3 lantiq: fix io_space_limit
5550d98015 ramips: fix kmod-sound-mt7620 packaging
489efcfd62 bcm53xx: refresh kernel config
7c02ecdd35 Revert "ar71xx: enable flow control for ethernet MACs with built-in switch"
9b4f17593a brcm47xx: add the small_Flash feature
44e6c0f916 ath25: add the small_Flash feature
30acacb0af config: add a small_flash feature
d57990e071 lantiq: fix ARV452CQW button gpio setup
d5143a49b7 lantiq: add AVM image mageic to sysupgrade script
abc346db0e package/lantiq: make lantiq kernel modules work with xway_legacy
239ad94165 lantiq: add xway_legacy target
2ae06f3013 lantiq: gpio-export fails to build if GPIO_SYSFS is not enabled
6ccf400be1 fstools: split snapshot-tool into its own package
fd7e15d493 fstools: remove bogus warning in the fstab script
4260d11e8b openvpn: update to 2.3.11
f869ffdd62 ar71xx: mach-ubnt-xm.c convert patches to mach file
6e0eccc5aa tools/firmware-utils: Add Archer C50 to mktplinkfw2
01fb393c67 ramips/image: Add Archer C50 to mt7620 Makefile
75af981239 ramips/base-files: Add support for Archer C50
1c00c09eb6 ramips/dts: Add support for Archer C50
bf007a480a lantiq: Add Support for Fritz!Box 7360 SL
8bd02b1381 strace: add option for enabling stack trace support
987f14ab23 libunwind: initial version 1.1
9a4935687d ramips: add support for DuZun DM06
49b7421836 ramips: enable wm8960 kernel menuconfig select option
6f61990d15 ramips: add i2s clocks
921d782eb7 ramips: update i2s dtsi files
9ff8928bb9 ramips: improve i2s drivers
42bbe28cf1 ramips: add i2c clock
011ce1fad6 ramips: update i2c dtsi files
d8202a8409 ramips: update i2c drivers
f36d624d88 ramips: add gdma hsdma dts info
f6fc591561 ramips: enhance dma engine support
3bb5f795d1 feeds.conf.default: disable management feed
9ba0dc602f ubox: update to latest git HEAD
c5bbb55bab toolchain/gdb: Use correct folder name for ARC patches
1f0a9715d2 package/devel/gdb-arc: Add target GDB for ARC
8cc65914df ipq806x: move dts file to the files folder
46cecfd6d7 ipg806x: set v4.4 as default
53147c2237 ipq806x: add mangle bootargs options in config-4.4
3d067c0132 ipq806x: base-files: add support for Linksys EA8500
2adc6468bf ipq806x: build Linksys EA8500 images
bdaf558134 ipq806x: qcom rpm fix support for smb208
928163bad2 uboot-envtools: add ipq806x support
2177a2a8cb mtd: add linksys_bootcount for ipq806x
c354591d1b mac80211: ath10k fix otp check patch
b50b0cff2d lantiq: use new property name for eiu irqs
d61af50cf3 lantiq: fix a regression in the eiu irq loading code
027da34957 lantiq: add default lan setup to board.d script
62dc9831d3 package/*: update git urls for project repos
399d214d05 oseama: support extracting entity
cb0de9a68e bcm53xx: sysupgrade: move TRX specific code to separated function
1beb5bec64 ar71xx: enable flow control for ethernet MACs with built-in switch
c536da365b lantiq: add VLAN handling fixes to xrx200 ethernet driver
172eebbd28 lantiq: fold 0400-xrx200-net-multi-phy.patch into 0025-NET-MIPS-lantiq-adds-xrx200-net.patch
233ec51217 ath10k-firmware: add QCA9984 firmware
5610afe203 sparse: update to support llvm 3.5.0
0aa6c7df60 kernel: update kernel 4.4 to version 4.4.13
1da87516e5 lantiq: change xrx200 ethernet driver WRED signal to global to fix spurious packet loss issues
704965d93f uboot-envtools: add config for WBMR300 (lantiq)
37cfc23cb7 kernel: require admin permissions for swconfig set operations
fecd715ef8 kernel: merge pending fq_codel backlog accounting fix
df7af9317b ath10k: merge some pending stability fixes
69c99a423a lantiq: enable swconfig LED support
cc3bfdb62f lantiq: enable SMP for XRX200
2d48f93ff4 lantiq: add Buffalo WBMR-300HPD support
cc87d144e1 lantiq: refresh xrx200 kernel config
2cf67832ec lantiq: remove dummy ltq_machine_power_off to fix gpio-poweroff drivers
eed2f24c0d kernel: fix mips MT_SMP kernel crash on cache flush
9e45f9d63c polarssl: enable AES-GCM and CAMELLIA-GCM ciphersuites
1f86257c2f bcm53xx: pass datasize to mtd in hexadecimal format
4b03e4ac3b mtd: fix typo in error message for 'c' option
c40e96d133 bcm53xx: fix partition typos in 09_fix_crc
442db0d6d8 kernel: deny swconfig set requests for unprivileged users
dd182011e1 swconfig: improve failure reporting
e815036460 dnsmasq: support hostid ipv6 address suffix option
4b8f0a2d26 mac80211: fix calculation of VHT capability values
96db69bd45 busybox: Call ntpd hotplug script for every action
7eaacd4d23 dnsmasq: Add option --max-port
95d8568cb8 bcm53xx: calculate TRX CRC32 using whole kernel partition
13ea815b6c mvebu: add a patch to deal with excessive latencies/delays during flash PIO command processing
a88fc0db9d xtables-addons: add missing dependency
efa740b08b ubox: increase default size of system log buffer to 64 kB
df7581e4c0 base-files: increase default system log size to 64 kB
0691a172d0 brcm2708: fix another missing kmod dependency
09f0850ba8 brcm2708: fix missing dependency found by buildbot
3fc661a98c brcm2708: update linux 4.4 patches to latest version
c17f02d2f2 brcm2708-gpu-fw: update to latest version
ece009dbf1 brcm2708: take over maintainership
67f0c93e28 kernel: add missing config symbols for 4.4
35b33f0413 base-files: maintain LED config state
98d418e05f brcm63xx: improve image/Makefile
d6ad9d3e9c base-files: fix /bin/config_generate breakage
57343b210a uboot-lantiq: get rid of bogus profile dependencies
924302ba36 base-files: drop /etc/config/system
b98f78b1c1 base-files: rework config generation logic
82768561c4 adm5120: remove target specific /etc/config/system
4f65b6f567 adm5120: convert LED setup to board.d
07f03d0833 base-files: support port_state LED types in board.d
197c32e7bd xburst: remove target specific /etc/config/system
168ba1a28e xburst: add /etc/config/system overrides via board.d
528b8f6f93 base-files: support hostname and ntp servers through board.d
a2e309a430 ath25: remove target specific /etc/config/system
0a3d721465 ath25: drop target specific button hotplug
7509658220 generic: remove brcmfmac-sdio.h
652ac2c6fd xtables-addons: update to 2.11
20c608db0a openvpn: add support for tls-version-min
33a4d22f4c base-files: reset LED state
21ad25f547 image.mk: fix dependencies for legacy make prepare step
24a7ccb056 treewide: replace jow@openwrt.org with jo@mein.io
e61fe4e4d7 ar71xx: add support for OpenEmbed SOM9331
69b45d2223 ixp4xx: fix Avila SoC audio driver compilation
160913f9de image.mk: fix filesystem dependency issue
97e3d10df9 lantiq: fix image DEVICE_DTS handling, add proper default value
821ccd2b36 lantiq: only call Image/Prepare/Profile for defined profiles
9b118cde89 wolfssl: enable openssl 1.0.1 compatibility
d84bf324ba ustream-ssl: update to the latest version, adds cyassl/wolfssl fixes
7eeb254cc4 treewide: replace nbd@openwrt.org with nbd@nbd.name
f7fb6e49f2 build: allow to build LEDE on latest MacOS X
4c5a49031e ar71xx: convert OM2P to device profile
26c771452c image.mk: add LegacyDevice wrapper to allow legacy image building code to be used for device profiles
ec86d2a605 ar71xx: enable profile sorting in preparation for adding device profiles
6036768d46 kirkwood: install kernel binaries into bin/ for use with external storage
f6c3f830a0 oxnas: install kernel binaries into bin/ for use with external storage
dafda4b7f8 image.mk: change the default of the kernel suffix
b50dfd5622 image.mk: add support for specifying a different suffix for the initramfs kernel
febc6cc5bf x86: lift generic x86-32 target
6c2fc113f3 x86: reorganize x86_32 support
4c33bbf8f4 image.mk: split off all Build/* commands into image-commands.mk
f8ebbbc568 build: implement support for selecting multiple device profiles
9ae952cf8c build: split scripts/metadata.pl into target-metadata.pl and package-metadata.pl
1a3c56f832 kmod-sched-cake: Add support for cake qdisc
23147dd43a iproute2: Add support for cake qdisc
bf89f5404b sunxi: remove NAMESPACES config symbols
d0ef9b4d38 mpc85xx: remove unneeded symbols
ac765cfdc8 zynq: remove unneeded _DIAG and _XFRM symbols
8f6df9465e sunxi: remove XFRM_ config symbols
34a3ec9c63 modules: add missing module to ipsec description
1b48152a63 oxnas: remove unneeded _DIAG symbols
c25541c024 malta: remove NAMESPACES config symbols
3ef433c2c0 malta: remove unneeded symbols
7cc4fa1ae1 procd: fix file permissions of /dev/tty* nodes
563e9d5e1b ar71xx: add WRTnode2Q support
754565a84b netifd: update to the latest version
699f7ecd15 x86: use sysfs DMI information to populate sysinfo
b8b23e0e64 x86: enable DMI and DMI_SYSFS
bd657ec9ac mediatek: remove modules from Kernel config
5d8ece87a4 util-linux: fix scanf fallback detection for uClibc-ng
8ee30ade17 ipq806x: add diag.sh script
ba42c1db41 lantiq: un-macro the image building code
f02184cbcf ubus: update to latest git HEAD
065de8bd7a ramips: fix Netgear EX2700 images
8b0fbd8e70 ramips: rebrand Netgear EX2700 fakeroot uImage
668dbec3f4 arc: Build uImage as well as vmlinux output files
9363259abe procd: update to latest git HEAD
1616bb2a7d lantiq/image: move tplink specific image into own file
aa930ba3dd lantiq: unmacro tp-link boards
35c0328119 kernel/mtd: Add support for Macronix mx25u25635f, used in Archer C2600 v1.1
d0c6458339 ixp4xx: Drop linux 4.1 support
2ce19c0c1f ixp4xx: Add support for 4.4 kernel, refresh patches
a0ea3eab63 brcm63xx: fix typo image/Makefile
3ec4803932 mac80211: respect user-set regulatory domain by default
56b377304e ath10k: support CT firmware choices.
532c3f3218 brcm63xx: add initial support for Netgear EVG2000
a529b41cff brcm63xx: set DSL-274XB-F1 ath9k LED as active high
85a0a908e3 brcm63xx: set HG556a A/B ath9k LED as active high
7807c7e867 brcm63xx: add support for inverting ath9k LED polarity
ec95509af4 brcm63xx: remove obsolote preinit scripts and fix preinit iface script
c69903473b brcm63xx: move profiles definitions to image/Makefile
2dc7f99662 brcm63xx: refresh kernel patches and config
fd7786159d brcm63xx: drop linux 4.1 support
23273044a8 brcm63xx: switch to linux 4.4
29b412b8c5 ramips: add kmod-pwm-mediatek for mt7628/mt7688
604b92dbd0 ramips: fix the number of uarts for each SoC
243e79e10c ramips: fix Mi Wi-Fi Nano Wireless LED pinmux
297142464a kernel/spi: add kernel package for spi-omap-24xx
49cf356710 kernel: add random-omap rng for omap
9efbf58360 omap: switch to 4.4
21208f5d43 linux/generic: add missing config symbols
51f05b2d1a omap: take over maintainership
a105eac4dd kernel: update kernel 4.4 to version 4.4.12
794383b801 brcm63xx: fix F@ST2704V2 image generation
9128ed33b5 add usb gadget ehci debug driver
2e980479c1 IB/SDK/toolchain: use lower cases filenames
4a7c653400 IB/SDK/toolchain: use VERSION_DIST_SANITIZED instead of VERSION_DIST
a7d13178f4 include: move VERSION_DIST_SANITIZED to version.mk
38d845b405 include: rename DIST_SANITIZED to VERSION_DIST_SANITZED
2a9f03adea ar71xx/image/edimax shorten the revision to 13 character
65ae9db41a brcm2708: fix build error introduced in 2b4e5d47
83390271f9 jsonfilter: fix printing 64bit values
872075c761 elfutils: remove unrecognized config option
75dc12dac1 libpcap: remove unrecognized configure options
04cb722e9f openvpn: remove unrecognized option
3a085dcbe3 download.mk: use HTTPS for git.lede-project.org
b38296f2f6 ramips: add Widora-NEO board support
5770678122 mt76: disable build for linux 3.18
b08dbd3acf mac80211: disable iwlwifi build for linux 3.18
44b82ab77a libiconv-full: add license tag
5ac43d6ec2 px5g: add license tag
c7d6a924ac usbutils: add license tag
d2a91f9853 ar71xx: Fix TL-WR841N v11 LEDs, use separate machine
927ab9a262 gettext-full: prevent using emacs
1205e9a781 mediatek: more nand fixes
9dafab92bf ipq806x: add a default profile
1e152483de ipq806x: enable PM support
442ff3b34d busybox: run sysntpd at higher priority
2a589539ba ramips: fix Netgear EX2700 images
0fa01e25ed ipq806x: remove accidentially comitted file
21802f22f0 ipq806x: fix 3.18 support
2b4e5d478b kernel: remove a hack that was obsoleted upstream
492964e741 lantiq: Use correct macaddr generating logic for the DGN3500
8b321d45be lantiq: Fix macaddr-setting code on DGN3500 and possibly other devices
96ad827e17 lantiq: fix segfault inside ltq-adsl-app
8333a6d0ba lantiq: Reduce ugliness of ugly hack
e8780b643b lantiq: Use the correct SPI flash speed for the Netgear DGN3500
8241479605 tools/tplink-safeloader: split CPE210 from CPE510 profile
b7864453f6 ar71xx: switch ordering and template to improve readability
b232669d45 ramips: fix Netgear EX2700 images
d517d8691a kernel/mtd: Add support for Macronix mx25u25635f, used in C2600 v1.1
867c0cb237 kernel/mac80211: skip ath10k OTP check if caldata found
cd36d71655 ipq806x/dts: Add Archer C2600 DTS
7d963efc40 ipq806x/base-files: extract ath10k caldata
14515cc271 ipq806x/base-files: Add support for Archer C2600
98b50f0bef ipq806x/base-files: Add Archer C2600 LEDs and board
ef02e8967c ipq806x: Add Archer C2600 to image/Makefile
5e49c57956 ipq806x: Add support for linux-4.4
955c341d3b fw-utils/tplink-safeloader.c: Add support for Archer C2600
7eb1a7e956 include/image.mk: move build step tplink-safeloader to image.mk
0c920e3281 toolchain: uClibc: Bump to the most recent version 1.0.14
b2b917cd06 lantiq: do not build images which exceed the flash size
c065cb08db uboot-lantiq: VGV7510KW22 - remove NOR SPL leftovers
db66b157db lantiq: VGV7510KW22 - enable the IP101A phy
4d5db712e3 lantiq: VGV7510KW22 - fix pinmux configuration
b0a202ebdc uboot-lantiq: Add Arcadyan VGV7519 support
ecf10d3796 uboot-lantiq: vrx200 - lzma compress gphy firmware
8df4eb0b9b uboot-lantiq: vrx200 - add support for dual nor flash
a9f7586ad2 lantiq: VGV7519 - fix brn partition layout
28faa3f292 lantiq: VGV7519 - get mac address from board_config partition
1e395608cc lantiq: VGV7519 - add vlan support
1deab53d88 lantiq: VGV7519 - add second usb port
79d92bb7ac lantiq: VGV7519 - cleanup pinmux configuration
8a382f1221 lantiq: VGV7519 - remove/merge redundant parts in dts
f778cdd9c9 lantiq: fix ARV4518PWR01 network
cdff540623 mac80211: brcmfmac: return -ENFILE if interface exists
efcaa046b7 mac80211: change default SSID from Lede to LEDE
2a57a54d49 ramips: add backported MT7628 pinmux fixes
8372a7f922 download.pl: Rework URLs
c4879556fe kernel: fix dependency chain of kmod-igb
6c1eb4441e util-linux: fix breakage
7f69458296 base-files: rework postinstall uci-defaults handling
749d4b77bd util-linux: fix sfdisk
71e0ef3978 ar71xx: add GPIO pin for usb power switch for RouterBOARD 912
7d67f79cb5 mediatek: more mtd fixes
a42e84b2db lantiq: fix regression in VG3503J.dts
dc44b2bd62 procd: Update to latest head
1eac53ba92 mediatek: update mtd backport
4ed8e57fd9 sdk: remove redundant symbol declaration
9eeb267c06 sdk: stop shipping a .config
32ae0da2b7 iproute2: Use URL alias
6e7403e1e6 iw: Use URL alias
52836866c9 kirkwood: add missing kernel symbol
f6785e33a0 jsonfilter: allow empty paths
4d1c75c601 dropbear: Fix incorrect CONFIG_TARGET_INIT_PATH.
1012701014 x86: generalize partition discovery for sysupgrade
3193053df7 Centralize setting of all version info to include/version.mk
6707d9750a busybox: sysntpd - Support for NTP servers received via DHCP(v6)
2ac21bd793 dnsmasq: Set the default dhcp lease file and resolv file
d79f8909c1 sdk: Allow to change ALL* package settings in SDK
76d8f6c41f usbutils: Use github alias
a6e96998fb dnsmasq: update to dnsmasq v2.76
0cc58a0f98 conntrack: enable support for netfilter conntrack zones
af1e70b4a7 ramips: Add status led for Xiaomi MiWiFi Nano
bf6634339a ramips: fix timing issues when using MT7621 spi
e0b241bb48 scripts/download.pl: Use CDN for kernel downloads
4c4497ec0d package: spidev_test: update location for >Kernel 4.5
35782e104a mvebu: configure switch on WRT1200AC and WRT1900ACv2/S
bf27ac019c ar71xx/cpe510: use second wifi calibration table
c5ff273d85 ar71xx/cpe510: split profile into 2 profiles cpe210 and cpe510
ce63c38ef5 image.mk: remove obsolete SUBTARGETS variable
f21de7d9a8 ar71xx: add MR1750v2 to the MR1750 profile
c4e3706533 ar71xx: extract ath10k wifi board.bin for the OpenMesh MR1750v2 board
3f508fce77 package/uboot-envtools: add OpenMesh MR1750v2 support
e1357c09d4 package/om-watchdog: add OpenMesh MR1750v2 support
77cb985022 ar71xx: enable sysupgrade for the OpenMesh MR1750v2
58dc285cd6 ar71xx: add user-space support for the OpenMesh MR1750v2
f7719dca71 ar71xx: add kernel support for the OpenMesh MR1750v2
634f681da4 ar71xx: add OM2P-HSv3 to the OM2P profile
00943e0931 package/uboot-envtools: add OpenMesh OM2P-HSv3 support
f3ac61850d package/om-watchdog: add OpenMesh OM2P-HSv3 support
222dfb3d6a ar71xx: enable sysupgrade for the OpenMesh OM2P-HSv3
e10d12411c ar71xx: add user-space support for the OpenMesh OM2P-HSv3
8010e8a370 ar71xx: add kernel support for the OpenMesh OM2P-HSv3
823cea2d5d ar71xx: Allow OpenMesh CE images with more than 3 files
d1b4a8cfcf ar71xx: Move OpenMesh image target validation into subfunction
6150c15ad1 ar71xx: Generate sysupgrade images for OpenMesh devices
9b6b75d09d ar71xx: Add support for initramfs images for OpenMesh devices
f85e5e6778 ar71xx: move nand device image definitions to a separate file
dcc2ea3cf5 ar71xx: move generic device image definitions to a separate file
054df4fda4 ar71xx: split ubnt image building code into a separate file
736fc38d33 ar71xx: split legacy image building code into a separate file
64b8bb3b69 ar71xx: split tp-link image building code into a separate file
0fd183c155 x86_64: enable mmc to support booting off sd
f89a20a89a ath25: update kernel from 3.18 to 4.4
c7efbd7dbb ramips: Add specific compatible properties for esw
f5f173e2b7 mediatek: update patches
a39ac242cc base-files: fix some failsafe issues
5dc80cbcff fstools: update to latest git version
12a24b6564 procd: update to latest head
abfdddfb3c lantiq: VG3503J - use the 11G firmware
9d0608eef3 lantiq: VG3503J - merge profiles
e81acacaa3 uboot-lantiq: ARV752DPW - use correct switch driver
a22feb4c78 uboot-lantiq: VGV7510KW22 - use ddr ram params from brnboot
382282eca9 uboot-lantiq: VGV7510KW22 - use leds to indicate boot status
9e8edcff99 uboot-lantiq: VGV7510KW22 - cleanup board config
b3795d0c93 uboot-lantiq: reorder and rework patches
74b1687be3 uboot-lantiq: drop unused board patches
21bdd79b33 lantiq: disable phy led complex (test) functions by default
9e41c3f54e imx6: move profile definitions to the image/Makefile
2965430999 ramips: cleanup for Hame MPR-A2
31293752c8 mdns: update to latest git HEAD
e00770f093 image.mk: fix profile selection in the image builder
df98acc6a1 mvebu: backport upstream ethernet driver improvements and enable buffer manager support
e90245237c oxnas: use global UBIFS_OPTS, all profiles use the same settings
2c9c998b4a mwlwifi: remove the a-mpdu failure messages entirely instead of hiding them in the debug log
848cacb21d mvebu: fix device I/O coherency issues
638a5682e1 kernel: remove bogus CONFIG_LOG_BUF_SHIFT overrides
a080b10331 mvebu: correct patch name of the crypto sram fix
629636dd25 mvebu: fix bus ranges for the crypto processor sram
7ae6b912ae libpcap: set a static default for PCAP_HAS_USB
22cc151e93 mvebu: tune kernel config for performance
f849c2c832 mvebu: enable core drivers in the kernel config instead of packaging them
a5a3b59bf5 mvebu: add some more flash driver fixes
008579f2ff mvebu: rename recently added flash driver fix
4926e4b1ae mwlwifi: fix excessive logspam if starting a BA session fails
29ad4d2a0c mwlwifi: fix excessive use of busy-waiting that was tripping up the flash driver
ab5e07f731 mwlwifi: update to 10.3.0.17-20160520-1
f0dd81043c mvebu: prevent crash in the flash driver in case of a spurious interrupt
566343246f mvebu: backport an upstream NAND flash driver fix
5166732a4e ramips: use green power LED as status indicator for Buffalo WSR-1166 and WSR-600
80bb5adf98 build: allow whitespace characters in VERSION_DIST
b570c0c88e uhttpd: use configured distribution name for SSL certificate CN
72568ea3bd ar71xx: remove linux 4.1 support
de27a1adae cyassl/wolfssl: update to 3.9.0
48ff6eff8c mac80211: add missing config symbols to PKG_CONFIG_DEPENDS
1050a609cf nvram: install init.d quirks script on brcm47xx only
8998dc14a5 brcm2708: fix SUBTARGET checks for bcm2709/bcm2710
24b8d31bad mvebu: update to linux 4.4
8eab383782 mvebu: fix portability issues in the image makefile code
0d476971f2 kernel: define CONFIG_CPU_THERMAL in kmod-thermal
d01487e380 image.mk: simplify device profile check, prepare for supporting selecting multiple profiles
c4ae33b048 image.mk: fix evaluation order for image profile check
cf58007abc bcm2708: explicitly check for SUBTARGET instead of using the device SUBTARGETS variable
c115058669 libubox: update to the latest version
323d37cbb6 arm64: update to linux 4.4
647e6379af kernel: add missing config symbols for 4.4
82dcbec727 ramips: remove fake vlan rx offload from ethernet driver
94e23bf740 ar71xx/cpe510: enable LNA for CPE210/220/510/520
118b5ae7b2 oxnas: drop compatibility with old kernels from mach-ox820
97ce23c347 oxnas: drop compatibility with old kernels from pinctrl
f90f379a7f oxnas: drop compatibility with old kernels from irq-rps
53a9809080 oxnas: drop compatibility with old kernels from dwmac-oxnas
c43635bc5c oxnas: sync 010-arm_introduce-dma-fiq-irq-broadcast with cns3xxx
c4664b0f91 kernel: update kernel 4.4 to version 4.4.11
d354bfde17 toolchain: Bump ARC tools to arc-2016.03
8d105653b1 base-files: sysfixtime typo in exclude dnsmasq.time
1ea7dba377 image.mk: fix building ubifs images
2c83003143 kernel: fix unaligned access issue in the bridge multicast-to-unicast patch
24270e9493 mac80211: fix unaligned accesses in the tx path
3bc90f9626 ramips: use backported upstream patches
1d0d5ddb07 curl: remove axtls config option, the library does not exist in our tree
6aebc6b16b curl: update to 7.49
9d37095fd0 ar71xx: fix a remaining unaligned access issue
934daa7b50 kirkwood: move ubi/ubifs options to the image makefile
311faaa1bd lantiq: move ubi/ubifs options to the image makefile
f2220bc1fe perf: disable libcrypto dependency
7938e8d60a dnsmasq: sysupgrade hook to conditionally preserve dnsmasq.time
2b1556d3e0 base-files: sysfixtime exclude dnsmasq.time
85a59127a7 Revert "dnsmasq: sysupgrade hook to conditionally preserve dnsmasq.time"
21f460e0c1 Revert "base-files: sysfixtime exclude dnsmasq.time"
9fd8e55132 imagebuilder: Fix sorting package list breaks opkg dependency handling for provides
d830cb0882 dnsmasq: sysupgrade hook to conditionally preserve dnsmasq.time
382779e009 base-files: sysfixtime exclude dnsmasq.time
c19b7aaac5 script/symlink-tree.sh: Fix missing config dir
3e08637e87 mdadm: Fix missing conffile and add initscript
3015af9647 ca-certificates: Add certificate bundle package
83049ed944 kernel: Build it87 hardware monitor module
638d509817 ramips: fix pinctrl regression
29db5cae43 ramips: fix spidev generic nodes
98204836a4 ar71xx: fix register address calculation for DDR flushing
021c893658 ramips: fix size-cells on spi nodes
b8a129638e kernel: add back the macronix software protection disable patch
21b04c623e ath9k: Fix TX99 support
262cec2fb8 mac80211: Allow selection of TX99 support in ath9k
01714243b9 bcm53xx: drop Copyright header from two of my bash scripts
2a6b899589 ramips: fix 8M WT3020 image creation
055d8d9c61 oxnas: move target-specific modules into target's modules.mk
17de501daa kernel: backport patches for fq_codel queue memory limit support
7bd10f9a2a image.mk: remove obsolete squashfs-lzma code
40f08abecf ar71xx: fix typo in pci memory window initialization fix
70eb03469f oxnas: reorganize image build code and nuke profiles
449aba4fe8 modules: hwmon: package driver for INA209 power monitor
910d9ba454 modules: hwmon: package driver for LTC4151 current sensor
2aa818a0bb kernel: add missing symbol
23a1fa07db libusb: disable parallel building
d4e552ba16 kernel: fix yaffs2 build with kernel 4.4
5521651863 ar71xx: typo in jjplus profile
470442ea0f build: fix make download in the SDK
34b05087f7 mac80211: fix a module build/dependency issue that was breaking lib80211
474d62e31d fstools: update to latest git HEAD
94cc41632e procd: update to latest git HEAD
1d9c0b2409 ramips: fix ArcherC20i image creation - 3rd try
acd7a34494 kernel: enable CONFIG_PANIC_ON_OOPS by default
2ecf3af576 kernel: set CONFIG_PANIC_TIMEOUT by default
f4c4d501e4 build: remove profile kernel/build system config override support
7a67b0e362 ar71xx: update to linux 4.4
9c556fe73e ar71xx: register the gpio driver earlier
313474e693 ar71xx: fix a PCI initialization issue in Linux 4.4
5b34dffcbd ar71xx: fix DDR write buffer flushing issues with 4.4
e30608b736 iw: refresh patches
df93d53a4b mac80211: update to wireless-testing 2016-05-12
ace946152d image.mk: fix emitting profiles for targets that have no subtargets
ce21e18d57 kernel: fix a compiler warning on 64 bit systems
ce009d16a1 ramips: fix Archer C20i image build
0b45bec22c ar71xx: add support for TP-LINK TL-WR842N/ND v3
5d0eff9801 ramips: set default profile to priority 1
cc831e23e1 ar71xx: add proper support for Archer-C7 V2
7697aced24 ramips: fix ArcherC20i image creation
27dfe64887 ramips/mt7621: remove cflags override
4d29474e26 target.mk: add cflags for mips 1004kc cpu type
bceafad7c2 kernel: add missing config symbol
d742e1b513 base-files: Enhancements to /etc/profile
424a94d81a brcm2708: convert to the new building system
20b069c440 ramips: disable unused ethernet ports on VoCore
f8abb68e3a tools/cmake: bump to 3.5.2
b4c286fa89 nettle: update to 3.2
e8bc0834e7 scripts/ipkg-build: fix deprecated GZIP environment variable warning
b40c22630f e2fsprogs: update to 1.42.13
da0226fa7e lua: Fixed broken __lt/__le operators caused by lnum patch.
45e0f8b826 arm64: add missing kconfig symbol
80f4988da3 target/imagebuilder: fix using new device profiles
0d10ada19c scripts/metadata.pl: add support for generating profile make code for the image builder
111285e742 download.pl: use http://sources.lede-project.org as download mirror
1c61b21489 dropbear: update to 2016.73
fad8bdfa40 kernel: backport patches improving fq_codel drop behavior
26c137621f kernel: remove out-of-tree patches for reducing qdisc truesize
75b069f505 kernel: fold codel default fix into main patch
7fab5dc486 ramips: fix indentation of Build/* template commands
98010ab489 kernel: remove ocf support, cryptodev-linux should be used instead
3d6d5ccf59 openssl: replace ocf-crypto-headers with a header file from cryptodev-linux
f816472f78 ar71xx: Fix TP-LINK Archer-C5/C7 v2 rfkill
d0edce233d README: Update project README
f10d2bb6d3 ramips: add wmac nodes to all mt7628/88 dts files
8c9b8d70b1 ramips: add status led for ZBT-WE826
4220cc3255 ramips: convert mt7620 to new image building code
ecbaaa401a ramips: convert mt7688 to new image building code
0f12f32996 ramips: convert mt7628 to new image building code
825717d450 ramips: convert mt7621 to new image building code
a55f0c32fa ramips: convert rt2880 to new image building code
34b6c8b075 iperf: Drop single-threaded variant
b4a23f83f9 iperf: Upgrade to version 2.0.8
8307c2fe68 ar71xx: Add support for Ubiquiti UniFi AP AC PRO
c855e70491 ar71xx: Rename unifiac to unifiac-lite
ffaaa6788a ramips: DTS modifications
b8ab6af1a9 global: change my email address
e1041e1bc0 ipq806x: enable fpu
e288e1bd32 kernel: fq_codel match flows_cnt to limit sizing
374cae9e6f ramips: add initial support for SamKnows SK-WB8
9195d8da35 ramips: DTS rework
861266c9ec dropbear: Add --disable-utmpx again
6a5471231b libusb: remove stale patch
05459a004a kernel: move the old gpio watchdog driver from generic to brcm47xx
30cd012860 gemini: delete 3.18 support
3f1705d777 bcm53xx: delete old kernel versions
b9c6361d5f mxs: delete old kernel versions
be83f982a7 sunxi: delete old kernel versions
930195737a oxnas: delete linux 4.1 support
825ef34f15 x86: remove defunct etherboot image building code
900b4865b8 x86: remove obsolete Config.in file
42d2eb7628 build: remove leftover dependenices on TARGET_rdc
cebc410d02 x86: remove rdc specific kernel patch
ac780e3ac8 tools/firmware-utils: remove obsolete firmware utility for airlink 525w
2e5f84fc10 x86: remove legacy script/makefile code for rdc devices
ca12fd431d x86: remove obsolete modules.mk
018807ded3 x86/xen_domu: enable xen drivers in the kernel config instead of packaging them as modules
303a241478 x86: enable grub at_keyboard support for x86_64
7d7fb75df5 x86: remove the kvm_guest subtarget
959bc143a0 x86/64: add more hardware RNG drivers, including for virtio
167404ceb5 x86/64: enable virtualization support for spinlocks to improve kvm performance
bc0ea9c273 x86: remove maintainer override for x86_64
dee8986b95 x86: remove the ep80579 subtarget, it has been unmaintained for a long time
d02f109ee4 kernel: remove leftover kernel version for 4.3
46b79085b6 busybox: fix issues with the ip command on mips64
26898d2a7f fstools: update to latest git revision
33d9d6c375 kernel: add workaround to rebuild vdso-n32.so.dbg too
e32b2f92b1 kernel: update kernel 4.4 to version 4.4.10
e042e0d50f kernel: remove linux 4.3 config
4a31037a34 build: avoid including profiles/*.mk
b0cf769008 image.mk: include per-device profiles in image build profile check
91799d5198 metadata.pl: fix target profile sorting check
15f88192bf ncurses: add a compatibility symlink for packages searching for ncursesw/ncurses.h
471ca4197c toplevel.mk: rescan target metadata if the image makefile changes
1189af85fd metadata.pl: add support for forcing sorting of profiles
87550a0e87 target.mk: dump device profiles defined in include/image.mk
6ddca3a361 target.mk: remove the unused Target-Path field
60fc6610be image.mk: add support for limiting images to specific subtargets
bcf67b6974 image.mk: prepare for defining device profile data in the Device section
40f933d7ff base-files: Fix config_generate when there are no switch VLANs or ports configured in board.json.
a3531f1986 README: Remove outdated info
f9a3123bbf netifd: Remove hardcoded DHCP release option
ef6d6661e2 ncurses: install a dummy libtinfo.a for packages that try to link it
cf3da7d204 Revert "ncurses: package the tinfo library separately"
30d955a7a5 build: fix make clean, delete package directories for selected arch
b9afc86b5c mtd: imagetag: fix compilation with changed mtd_fixtrx call
86777a40e9 gettext-full: avoid spurious dependencies on ncurses
975f7160dd ncurses: package the tinfo library separately
f6059cc118 ramips: fix DTB generation
fda951c443 iftop: Update to latest version, and drop patch
b01f296f4f ncurses: provide libncurses compatibility symlinks in libncursesw
f8b6c9d825 ramips: Change all '/include/' clauses to '#include' so preprocessing can be done properly for the entire device trees.
600c224213 ramips: Add hex prefix (0x) to dtsi reg properties where needed.
b8f73d7f0a ramips: introduce serial0 aliases
b062266ad6 kernel: update kernel 4.4 to version 4.4.9
a4571b7631 ubox: make logging code honour the hostname properly
c3cf3c4ec4 brcm47xx: fix wgt634u port assignment, broken since openwrt r47866
823c58a1cf ramips: mt7620: [UPSTREAM] fix USB frequency scaling
1570277094 ramips: Fix alphabetical sorting for 02_network
39f035fdc7 ramips: Don't use a VLAN for the single ethernet port of the A5-V11.
ffb7bf7672 ramips: Fix network for routers without VLANs on eth0.
40bfe9f0bd ramips: Drop hacky switch workaround for failsafe on rt3x5x and rt5350.
3f638902b6 ramips: Disable all ethernet ports except port 0 on A5-V11.
d5114b509b ramips: Disable all ethernet ports except port 4 on HT-TM02.
12758e32d3 ramips: Get rt3050 ethernet ports to be disabled from the device tree.
e626d4f702 ramips: Fix comment in rt3050 ethernet switch driver.
e716fce5da ramips: Fix documentation for the rt3050 switch driver.
decd89c57f ramips: Fix multicast ICMPv6 for the rt3050 ethernet switch.
75629fb2a8 ar71xx: add TP-Link TL-WR810N support
cbdfae5c04 ubox: turn logd into a separate package
d4de9f72f3 lantiq: VGV7510KW22BRN - set the phy clock source
44cace4dab lantiq: add device tree binding for the phy clock source
60ac485274 lantiq: VGV7510KW22BRN - support dual-image
d7438ce315 lantiq: handle the dual-firmware layout of brnboot
b7fc892eb5 lantiq: move partitions into partion table node
b695ce2999 lantiq: use sysupgrade.bin postfix for tplink images
5ed2140162 lantiq: VG3503J - use the same PHY led functionality as the OEM firmware
ba3ed629ea ar71xx: Fix eth0 support for Ubiquiti UniFi AP AC
b529387d8c lantiq: use the same functionality for all ethernet phys led
6249269322 lantiq: fix minor typos in 11G/22F phy driver
6b0425a187 ramips: add support for Planex MZK-EX750NP.
23596ca527 mediatek: sync patches and add more ethernet stability fixes
dd16b7748d ncurses: install pkg-config files to fix util-linux build breakage
df8ca9a5c4 mtd: add -c option for specifying amount of data to be used for checksum
2dd125048d mtd: trx: use separated buffer for TRX header
6de401b1f8 mtd: seama: exit with error if Seama header wasn't found
06a3241c27 mtd: seama: fix image data handling
30edc32888 mtd: seama: move buf allocation to the MD5 function
1d628f0cbe mtd: seama: update MD5 using header in the first block buffer
bcccb03200 mtd: seama: add md5 to header struct
8632d89fa0 mtd: check for Seama magic early when fixing MD5
320641585b mtd: add missing breaks in a switch
8a60a41951 mtd: use tabs for indents
5071fb27b9 ncurses: remove libncurses, provide it via libncursesw
4a3348ef09 metadata.pl: add support for selecting packages available only via PROVIDES
91f205acaf kernel: add workaround to rebuild vdso-o32.so.dbg
3339f14e84 toolchain: gcc: fix build with GCC 6
c7e2a89a4d tools: mkimage: sync include/linux/compiler*.h with u-boot master
741aa2a816 tools: pkg-config: fix build with GCC 6
5b64e3532a mt76: update to the latest version
6259583ef3 mt76: fix rebuild on CONFIG_PACKAGE_MAC80211_MESH changes
852aaf6b2c build: add support for specifying extra package dependencies for prepared, configured and built
4e84c6cbd2 toolchain: rename OpenWrt into LEDE
173ac3b7cb sdk: rename OpenWrt into LEDE
009a069ec0 imagebuilder: rename OpenWrt into LEDE
9ec4ca525c tools: make-ext4fs: fix build regression on mac os x
9b9c78e071 base-files: evaluate uci-defaults on run-time installations
f6adbdf3cd openssl: Update to version 1.0.2h
4076d863bd firewall3: fix mark rules for local traffic, fix race condition
a2b555189b libiconv: add all ASCII aliases
6a06cd8331 xtables-addons: Avoid redefinition of SHRT_MAX in lua packet script
a6f76bffd8 signing: remove unatteded build key and use current keyring instead
33de8c77e2 fstools: fix snapshot support
0fae7270cf fstools: update to latest git HEAD
4a8e960c62 base-files: fix group/user settings after sysupgrade
ed07ef1601 base-files: split user/group addition code into a function
797fb8a302 scripts: add "r" to revision
c9e3cd798d fstools: update to latest git HEAD
d72e538e89 base-files: add new public key used by unattended builds
a13f47760c base-files: add a conditional dependency to lede-keyring
d2e4caf343 lede-keyring: add the developer public keyring
f5c4d963ff include: add lede git server url
9eb155353a kernel: add a workaround to rebuild vdso.so.dbg after genvdso
d9a0a8c78f scripts: avoid hard-coded paths in scripts
ec9f6fe04d ppp: Add ppp-mod-passwordfd subpackage to ppp
ce9e5e16ff dnsmasq: Add conntrack support in the full variant
16122117a5 dropbear: Add procd interface triggers when interface config is specified
b3f6c4b3ac iproute2: Add package for nstat utility
7545c1d96b dropbear: Make utmp and putuline support configurable via seperate config options
a83f049b5b netifd: Add configurable DHCP release behavior
cf3b3cfc56 bcm53xx: add m25p80 workaround for SPI flash writing problems
090b134786 mediatek: sync and patches add support for several boards
9e4d671f75 bcm53xx: support SPI-NOR on dual flash devices
741715331a bcm53xx: switch to m25p80 and drop bcm53xxspiflash
73d51d7b5d bcm53xx: support JEDEC incompatible w25q128 in spi-nor
312cb987f9 xtables-addons: Fix Lua packet script implementation
eb529d2625 lantiq: fix xway image building
07bdd30906 package: remove duplicate lines from otrx and nvram makefiles
b04a25491f package: flag further target specific packages as nonshared
69ccef03f9 package: mark nvram and otrx nonshared as they're target specific
7df1964180 brcm2708: removes backported patch (linux-4.4.7)
f7a2237b86 at91: fix SAMA5D3 subtarget
ec5680a73d x86: remove old references to kmod-acpi-button
c0a287610a uml: revert accidentally committed change
49ad0c565a tools: fix make_ext4fs build with recent glibc
525b311bf8 brcm2708: update linux 4.4 patches to latest version
0ab31bfced brcm2708-gpu-fw: update to latest version
a90ee92337 kernel: fix ip6_tunnel compilation
3faf65e928 kernel: update kernel 4.4 to version 4.4.8
4c60a6f803 opkg: fix use-after-free with duplicate packages on the command line
b9466382b5 imagebuilder: use correct package directory when bundling kmods and libc
9531e0fce5 package: fix toolchain ipk flags
d9ad55a609 include: remove unused FeedPackageDir macro arguments
37de17c379 linux: kmod-e100: use preconverted firmware files
484cb91ad5 sdk: bundle required firmware files
1191eeff8e include: bin/ dir was not created
528ffec3cd base-files: remove ununsed login.sh
b4e33a1c08 base-files: Allow to disable failsafe mode
dc92917409 image / basefiles: make console password configurable
5e85ae9e4c base-files: fix error message during boot
f8ce7e028d sdk: do not exclude ccache executable
0f6f518e7a sdk: fix generation of base feed url
e885286834 target: globally remove ARCH_PACKAGES overrides
02def71888 include/target.mk: disambiguate package architecture
3339f41d26 brcm2708: implement sysupgrade image check
9dee77795d brcm2708-gpu-fw: improve package version and release
2cd1f5a0db brcmfmac43430-firmware: improve package version and release
e821fdbadb brcm2708: add missing config symbols
349e7b635e include: fix nonshared flag handling
abc828b085 openssl: fix wrong build target strings
addfc0efdd uclibc++: add hack to fix failing patch
da46d2b228 imagebuilder: fix standalone operation
9e04019024 package: flag essential components as nonshared
d87c303b58 include/kernel.mk: flag kmod packages as nonshared by default
32a0b8c104 include/version.mk: rework repository url handling
5170393f8c include: choose package output directory based on repository info
941fc5e8c8 global: introduce ALL_NONSHARED symbol
bf4bfd8ccc scripts: remove "Package-Subdir" metadata handling
be575fdc9d include: remove now unused PACKAGE_SUBDIR variable
9a04a80677 scripts: metadata: use the new "Repository" field
aad2b92603 include/package-dumpinfo.mk: introduce Repository values
c47abdea25 include/target.mk: default to CPU_TYPE for the package architecture
54fbe8afdd rules.mk: introduce new variable OUTPUT_DIR
7322cca9fa scripts: metadata: add CONFIG_TARGET_SUBTARGET symbol
a8d4d71c41 brcm2708: update to latest version
59e0e88c22 brcm2708-gpu-fw: update to latest version
f233664faa brcm2708-gpu-fw: update to latest version
8d5160bf5d brcmfmac43430-firmware: use @GITHUB download alias
694f060550 download: add @GITHUB download facility
5a7c064bdb busybox: fix setting the kernel timezone
81a5f1ac9e netifd: Send DHCP release when client exits
3df4eaf22b uci: commit through symlinks
564330e013 netifd: fix default ip rules
924fb794bd x86: search PARTUUID in any block device
9f422eba7c x86: make sysupgrade work without partx
fa69553900 branding: add LEDE branding
343c3be454 scripts/getver.sh: generate revision relative to the reboot tag
```

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

