Asuswrt-Merlin 384/NG Changelog
===============================

384.18 (28-June-2020)
  - NOTE: A number of changes for some models are not backward
          compatible with previous versions.  Downgrading to
          a previous release will require a factory default reset
          afterward in many cases.
  - UPDATED: Merged GPL 384_8563 for AX models.
  - UPDATED: Merged GPL 384_81918 for mainline models.
  - UPDATED: Merged SDK + binary blobs 384_81918 for RT-AC86U.
  - UPDATED: Merged SDK + binary blobs 384_81902 for RT-AC5300.
  - UPDATED: Merged SDK + binary blobs 385_20490 for RT-AC68U.
  - UPDATED: Merged binary blobs 385_20490 for RT-AC3100.
  - UPDATED: Merged binary blobs 384_81918 for RT-AC88U.
  - UPDATED: Merged SDK + binary blobs 384_8563 for RT-AX58U.
  - UPDATED: amtm to 3.1.7.
  - UPDATED: Root certificate bundle to June 3rd 2020.
  - UPDATED: OUI database used by the webui.
  - UPDATED: Dropbear 2020.80 (themiron)
  - UPDATED: nano to 4.9.3.
  - CHANGED: Optimized OpenVPN routing policy storage (this change
             is NOT backward compatible with previous firmwares)
  - FIXED: ssh/scp client would fail to connect while negotiating
           a chacha20 connection (themiron)



384.13_10 (28-June-2020)
  This release will most likely be the last release for the
  RT-AC87U and RT-AC3200, due to limited upstream support.

  - UPDATED: amtm to 3.1.7.
  - UPDATED: Root certificate bundle to June 3rd 2020.
  - UPDATED: OUI database used by the webui.
  - UPDATED: Dropbear 2020.80 (themiron)
  - UPDATED: Wireless driver from 382_52230 for RT-AC87U and
             RT-AC3200 (should in theory address Kr00k)
  - FIXED: ssh/scp client would fail to connect while negotiating
           a chacha20 connection (themiron)


384.17 (26-Apr-2020)
  Updating some models (like the RT-AC88U) from stock firmware
  3.0.0.4.384_81790 and newer will require a factory default reset
  after flashing Asuswrt-Merlin, due to a change in how Asus
  stores the admin password starting with 384_81790.

  - NEW: Add Chacha20-poly1305 support to dropbear (themiron)
  - UPDATED: dnsmasq to 2.81-openssl (themiron)
  - UPDATED: openvpn to 2.4.9.
  - UPDATED: curl to 7.69.1.
  - UPDATED: openssl-1.1 to 1.1.1g (themiron)
  - UPDATED: nano to 4.9.2.
  - FIXED: RT-AC88U/RT-AC3100/RT-AC5300 could fail to upgrade
           from newer stock versions to Asuswrt-Merlin.
  - FIXED: Various webui issues with sorting DHCP reservations.


384.13_8 (26-Apr-2020)
  This release is only available for the RT-AC87U and RT-AC3200.

  - UPDATED: dnsmasq to 2.81-openssl (themiron)
  - UPDATED: openvpn to 2.4.9.
  - UPDATED: openssl-1.1 to 1.1.1g (themiron)


384.16 (5-Apr-2020)
  - NEW: Added support for the RT-AX58U and RT-AX3000 (same
         firmware), based on GPL 384_8253 + binary blobs 384_8137.
  - NEW: Added support for the RT-AX56U, based on GPL + binary
         blobs from 384_8253.
  - NOTE: The RT-AC87U and RT-AC3200 are now officially considered
          to be on limited support.  The future for these two
          models will depend on Asus's own support in the
          coming months.

  - NEW: Added ed25519 support in Dropbear (themiron)
  - UPDATED: Merged GPL 384_8253 for AX models.
  - UPDATED: Merged SDK + binary blobs 384_7977 for RT-AX88U.
  - UPDATED: Merged SDK + binary blobs 384_81352 for RT-AC86U.
  - UPDATED: Tor to 0.4.2.6.
  - UPDATED: curl to 7.68.0.
  - UPDATED: nano to 4.8.
  - UPDATED: dnsmasq to 2.81rc4-33-g7558f2b-openssl (themiron)
  - UPDATED: inadyn to 2.7 (themiron, merlin)
  - UPDATED: getdns to 1.6.0 (themiron)
  - UPDATED: stubby to 0.3.0 (themiron)
  - UPDATED: amtm to 3.1.6 (thelonelycoder)
  - UPDATED: openssl-1.1 to 1.1.1f (themiron, merlin)
  - UPDATED: Chart.js to 2.9.3
  - CHANGED: Wireless Log page will now regroup Guest Network
             clients together and identify which guest instance
             they are connected to.
  - CHANGED: Report temperature of second 5 GHz radio on Sysinfo page
             for tri-band models.
  - CHANGED: Added down/upload monitor to network status page, and
             removed useless RAM chart to free some space.
  - CHANGED: Security hardening in dropbear dropped CBC and 3DES
             ciphers, removed version disclosure from ident
             string (themiron)
  - FIXED: DNS server was unreachable when connecting to an OpenVPN
           server with Advertise DNS enabled, due to firewall rules.
  - FIXED: Router Security Assessment would fail to recognize WPA3
           as being secure.
  - FIXED: miniupnpd would reject private WAN IPs - changed that
           upstream behaviour to allow these.
  - FIXED: Would require you to reset the DHCP scope if you
           changed the LAN hostname.
  - FIXED: Couldn't set http mode to http-only if you previously
           had WAN access enabled but have since switched to
           non-router mode.
  - FIXED: Disks with a single quote in their name would fail to
           properly list on various USB service pages.
  - FIXED: CVE-2020-8597 security issue.


384.13_6 (5-Apr-2020)
  This release is only available for the RT-AC87U and RT-AC3200.
  These two models are now considered to be on limited support, and
  their future will depend on Asus's future support for these two.

  - UPDATED: openssl-1.1 to 1.1.1f (themiron, merlin)
  - UPDATED: amtm to 3.1.6 (thelonelycoder)
  - CHANGED: Security hardening in dropbear: dropped CBC and 3DES
             ciphers, removed version disclosure from ident
             string (themiron)
  - FIXED: DNS server was unreachable when connecting to an OpenVPN
           server with Advertise DNS enabled, due to firewall rules.
  - FIXED: miniupnpd would reject private WAN IPs - changed that
           upstream behaviour to allow these.
  - FIXED: Would require you to reset the DHCP scope if you
           changed the LAN hostname.
  - FIXED: Couldn't set http mode to http-only if you previously
           had WAN access enabled but have since switched to
           non-router mode.
  - FIXED: Disks with a single quote in their name would fail to
           properly list on various USB service pages.
  - FIXED: CVE-2020-8597.


384.15 (8-Feb-2020)
  The RT-AC87U and RT-AC3200 are not supported by this release, see
  the 384.13_4 release released separately for these two models.

  - NEW: wan-event script.  The first parameter will be the WAN unit
         (0 for first WAN, 1 for secondary).  The second parameter
         will be a string describing the type of event (init,
         connected, etc...).  A wan-event of type "connected" will
         be identical to when the original wan-start script was
         being run (wan-start should be considered deprecated
         and will be removed in a future release)
  - NEW: Implemented an official API for addon developers to
         better integrate with the router.  This includes up
         to ten different pages that can be added anywhere within
         the webui, and a dedicated storage repository for your
         settings, which can be interacted with through your
         custom web page or through a shell script.
         See the Wiki for more information:

         https://github.com/RMerl/asuswrt-merlin/wiki/Addons-API

  - NEW: amtm (Asuswrt-Merlin Terminal Menu) by thelonelycoder has
         been added to the firmware.  Running "amtm" over SSH will
         give you a menu allowing you to select and install various
         addons, such as Diversion (ad blocker) or SKynet (an
         advanced firewall extension).  The plugins for amtm are
         still maintained by its original author (thelonelycoder).

         https://github.com/RMerl/asuswrt-merlin/wiki/AMTM

  - UPDATED: Backported some fixes from 384_81981, mostly related
             to WAN, port bonding and mdns.
  - UPDATED: Merged GPL 384_7756 for RT-AX88U, which adds OFDMA and
             WPA3 support to that model.
  - UPDATED: Merged with GPL 385_10002 for other models (from
             RT-AC68U)
  - UPDATED: odhcp6c to 1.1-97-ge199804 (themiron)
  - UPDATED: curl to 7.67.0.
  - UPDATED: openssl-1.0 to 1.0.2u
  - UPDATED: dnsmasq to 2.80-114-ge40d8be (themiron)
  - CHANGED: Replaced entware-setup.sh script with link to amtm, as
             using the amtm Entware installer is now the supported
             method.
  - CHANGED: Improved connection handling in httpd (themiron)
  - FIXED: Some of the newest DNSFilter servers weren't properly set
           up with IPv6 (dave14305)


384.13_4 (8-Feb-2020)
  This release is only available for the RT-AC87U and RT-AC3200.

  - NEW: wan-event script.  The first parameter will be the WAN unit
         (0 for first WAN, 1 for secondary).  The second parameter
         will be a string describing the type of event (init,
         connected, etc...).  A wan-event of type "connected" will
         be identical to when the original wan-start script was
         being run (wan-start should be considered deprecated
         and will be removed in a future release)
  - NEW: Implemented an official API for addon developers to
         better integrate with the router.  This includes up
         to ten different pages that can be added anywhere within
         the webui, and a dedicated storage repository for your
         settings, which can be interacted with through your
         custom web page or through a shell script.
         See the Wiki for more information:

         https://github.com/RMerl/asuswrt-merlin/wiki/Addons-API

  - NEW: amtm (Asuswrt-Merlin Terminal Menu) by thelonelycoder has
         been added to the firmware.  Running "amtm" over SSH will
         give you a menu allowing you to select and install various
         addons, such as Diversion (ad blocker) or SKynet (an
         advanced firewall extension).  The plugins for amtm are
         still maintained by its original author (thelonelycoder).

        https://github.com/RMerl/asuswrt-merlin/wiki/AMTM

  - UPDATED: odhcp6c to 1.1-97-ge199804 (themiron)
  - UPDATED: openssl-1.0 to 1.0.2u
  - UPDATED: curl to 7.67.0.
  - UPDATED: OpenVPN to 2.4.8.
  - UPDATED: dnsmasq to 2.80-114-ge40d8be (themiron)
  - CHANGED: Replaced entware-setup.sh script with link to amtm, as
             using the amtm Entware installer is now the supported
             method.
  - CHANGED: Improved connection handling in httpd (themiron)
  - FIXED: Some of the newest DNSFilter servers weren't properly set
           up with IPv6 (dave14305)


384.14_2 (1-1-2020)
  - FIXED: Missing cifs kernel module
  - FIXED: stubby was linked with OpenSSL 1.0 instead of 1.1
  - FIXED: some routers were reporting the Internet connection being
           disconnected.  If you were affected and you had flashed
           a customized bootloader, then please reflash your original
           bootloader, as your modded bootloader is invalid, and other
           potential issues may appear over time.
  - FIXED: Random traffic spikes logged in Traffic Monitor (regression
           from 384_81351)


384.14 (14-Dec-2019)
  - NEW: Implement option to prevent Firefox's automatic usage of DoH.
         By default, this will only apply if you have DNSPrivacy
         enabled, or if you have DNSFilter enabled with a global
         filter, to ensure that Firefox will not bypass either of
         these.  You can also have this override applied all the
         time, or completely disable it.
  - NEW: Added "split" busybox applet.
  - NEW: Added IPv6 support to Network Analysis webui
  - NOTE: You might need to reconfigure your device hostname on the
          LAN -> LAN IP page due to a GPL-level change (exclusing
          the RT-AX88U)
  - UPDATED: RT-AX88U to GPL 384_6436 (with Let's Encrypt fixes
             backported from 384_81351)
  - UPDATED: RT-AC68U, RT-AC86U to GPL 384_81351
  - UPDATED: RT-AC88U, RT-AC3100 to GPL 384_81351 and binary
             blobs from 384_81116
  - UPDATED: RT-AC5300 to GPL 384_81351 and binary blobs from
             384_81219.

  - UPDATED: miniupnpd 20190824
  - UPDATED: dnsmasq 2.80-95-g1aef66b (themiron)
  - UPDATED: OpenSSL 1.0.2 to 1.0.2t (themiron)
  - UPDATED: OpenSSL 1.1.1 to 1.1.1d (themiron)
  - UPDATED: Curl 7.66.0
  - UPDATED: nano 4.4
  - UPDATED: OpenVPN 2.4.8
  - UPDATED: OUI database to 2018-08-17 version
  - UPDATED: CA root certificates to October 9th 2019
  - CHANGED: Made webui SSL certificate generation compliant with
             IOS 13 and MacOS 10.15 new requirements.
  - CHANGED: Rewrote the faketc script used to inject Codel into
             Adaptive QoS as a C program for improved performance.
  - CHANGED: Moved /usr/bin/ip to /usr/sbin/ip on the RT-AC86U and
             RT-AX88U to match other models.
  - CHANGED: IPv6 firewall now accepts empty values for local IP
             (which means any local IP).
  - FIXED: Webui wouldn't notify when running dangerously low on
           free nvram (feature was lost at some point in the past)
  - FIXED: Non-working link to YandexDNS on the webui for
           Russian models.
  - FIXED: Backported various httpd fixes to RT-AX88 from other
           models.
  - FIXED: Custom clientlist would be wiped if stopping an
           OpenVPN server instance.
  - FIXED: Incorrect detection of EUI64 addresses on the IPv6
           firewall (would prevent using ::/0 for instance).
  - FIXED: EUI64 support missing while in Load Balancing or
           using Multicast IPTV.
  - FIXED: Asus DDNS failing to update due to an invalid
           certificate on Asus's server.
  - FIXED: Let's Encrypt support would sometime fail when using
           Asus DDNS (fixed DNS publishing of validation record)
           (in addition to general failure fixed by GPL 81351)
  - FIXED: IPv6 neighbour solicitation drop toggle not working
           for some models
  - FIXED: openvpn-event scripts would be executed even if custom
           scripts were globally disabled


384.13_2 (14-Dec-2019)
  This release is only available for the RT-AC87U and RT-AC3200.

  - NEW: Added "split" busybox applet.
  - UPDATED: OpenSSL 1.0.2 to 1.0.2t (themiron)
  - UPDATED: OpenSSL 1.1.1 to 1.1.1d (themiron)
  - UPDATED: CA root certificates to October 9th 2019
  - CHANGED: Rewrote the faketc script used to inject Codel into
             Adaptive QoS as a C program for improved performance.
  - CHANGED: Made webui SSL certificate generation compliant with
             IOS 13 and MacOS 10.15 new requirements.
  - CHANGED: IPv6 firewall now accepts empty values for local IP
             (which means any local IP).
  - FIXED: Non-working link to YandexDNS on the webui for
           Russian models.
  - FIXED: Webui wouldn't notify when running dangerously low on
           free nvram (feature was lost at some point in the past)
  - FIXED: Custom clientlist would be wiped if stopping an
           OpenVPN server instance.
  - FIXED: Incorrect detection of EUI64 addresses on the IPv6
           firewall (would prevent using ::/0 for instance).
  - FIXED: EUI64 support missing while in Load Balancing or
           using Multicast IPTV.
  - FIXED: Asus DDNS failing to update due to an invalid
           certificate on Asus's server.
  - FIXED: Let's Encrypt no longer working due to deprecated ACMEv1
           protocol usage (backport from GPL 81351)
  - FIXED: Let's Encrypt support would sometime fail when using
           Asus DDNS (fixed DNS publishing of validation record)
  - FIXED: IPv6 neighbour solicitation drop toggle not working
           for some models


384.13_1 (12-Aug-2019)
  - FIXED: RT-AC87U failing to boot when configuring in AP mode.


384.13 (31-July-2019)
  - NEW: AiMesh Router and node support.  Note that automatic live
         update of Merlin-based nodes is not supported, you will have
         to manually update any Merlin-based nodes when a new firmware
         is available.  Asus-based nodes (which is recommended) will be
         able to make use of the automatic live update.
  - NEW: ChaCha20-Poly1305 support in Strongswan (themiron)
  - UPDATED: RT-AX88U to GPL 384_6210.
  - UPDATED: Curl 7.65.3.
  - CHANGED: dhcp_staticlist no longer contains hostnames, these
             have been moved to dhcp_hostnames for better
             compatibility with upstream and closed source
             components, also allows more static leases to be
             defined before reaching the size limit.
  - CHANGED: Replace Nettle with OpenSSL for dnsmasq's DNSSEC
             validation, which opens the door to supporting
             more ciphers.  (themiron)
  - FIXED: Firmware Update check button would redirect to Asus
           support site if scheduled checks are disabled.
  - FIXED: Firefox was showing a no-op Uninstall button on the
           AiCloud page
  - FIXED: 5 GHz radio showing as disabled on the Sysinfo page for
           the RT-AC87U
  - FIXED: FTP would be accessible from the WAN even while disabled
           if you had DualWAN load balancing enabled, or IPTV
           configured.
  - FIXED: IGMP Snooper daemon crashing when more than 32 hosts
           are present (themiron)
  - FIXED: External DDNS IP checker would fail for Chinese users,
           as checkip.dyndns.org is blocked - switched to .com TLD.
  - FIXED: Devices without a networkmap-defined alias wouldn't fallback
           to their hostname on some webui pages like the IPTraffic
           and QoS Classification pages.
  - FIXED: Remote IP field filtering on Classification page wasn't
           working.
  - FIXED: Incorrect user permissions displayed on the FTP page.
  - FIXED: Performance issues for some users, following the kernel
           security fixes in 384.12. (gzenux)


384.12 (22-June-2019)
  - NOTE: The project now has its own domain name.  Official website
          is now https://www.asuswrt-merlin.net/ and my email address
          for anything related to the project is now
          merlin@asuswrt-merlin.net.

  - NEW: Added WS-Discovery support.  This allows Windows clients
         to detect the router's shared USB drives even if SMBv1
         support is disabled.
  - NEW: Re-added option to extend the WAN's TTL (from stock
         firmware, was previously disabled as it used to
         be broken)
  - UPDATED: RT-AC3200 and RT-AC87U to 382_51640/51634 binary blobs
             (with a few exceptions for 384_xxxx compatibility)
  - UPDATED: Merged GPL 384_45717 (except for RT-AX88U)
  - UPDATED: Nano 4.2.
  - UPDATED: OpenSSL-11 to 1.1.1c.
  - UPDATED: OpenSSL-10 to 1.0.2s.
  - UPDATED: curl 7.65.1.
  - UPDATED: miniupnpd 20190604.
  - CHANGED: Local clients will be shown by their hostname
             on the Classification page.
  - CHANGED: Reworked handling of up/down events in OpenVPN.
             Server instance will now also use its own
             updown script, which will handle firing up
             openvpn-event (if present).
  - CHANGED: Inbound traffic sent to you through an OpenVPN client
             will now be dropped by default.  This can be changed
             through the new "Inbound Firewall" parameter found
             on the OpenVPN client page.  You should only change
             this to "Allow" if running a site2site tunnel with
             a trusted remote server, or if you do expect
             traffic to be forwarded to you through the tunnel.
  - CHANGED: The router will now use ISP-provided resolvers
             instead of local dnsmasq when attempting to
             resolve addresses, for improved reliability.
             This reproduces how stock firmware behaves.
             This only affects name resolution done
             by the router itself, not by the LAN clients.
             The behaviour can still be changed on the
             Tools -> Other Settings page.
  - CHANGED: Randomize the serial number of certificates
             generated by the router for its httpd.  If
             using a router-generated certificate, then
             it's recommended to generate a new one.
  - CHANGED: Allow USB idle values up to 9999.
  - CHANGED: Replaced Network Analysis and Netstat pages (under
             Network Tools) with new versions based on Asus's
             Netool daemon for non-HND models, but based
             around the more limited traceroute busybox applet.
             RT-AC86U and RT-AX88U still use the newer
             traceroute executable.
  - CHANGED: Reworked how some services are started when the WAN
             interface comes up to prevent deadlocks between
             the WAN completing its initialisation, and the
             clock getting set.  These could result is fairly
             long boot time for some ISPs.
  - FIXED: openvpn-event script not launching if the
           client was configured in Secret Key auth
           mode.
  - FIXED: IPv6 issues on RT-AX88U - backported accept_ra fix
           from 45717 (themiron)
  - FIXED: Memory leak in erp_monitor process.
  - FIXED: Page redirection failing to apply at boot
           time if WAN was down.
  - FIXED: CVE-2019-11477, CVE-2019-11478 and
           CVE-2019-11479 (themiron)


384.11_2 (18-May-2019)
  - NEW: Implemented source/destination IP filtering
         for the Netool version of Netstat web page.
  - CHANGED: Backported multiple fixes and improvements
             for ntpd from upstream, improving handling
             of failed server hostname resolution, and better
             clock sync discipline.
  - FIXED: RT-AC88U/3100/5300 were accidentally compiled
           with Netool enabled, which isn't compatible with
           these model's kernel.
  - FIXED: Movistar stopped working for some users.  Re-disabled
           udpxy on Movistar profile for now.  A more complete
           fix will have to come from Asus.
  - FIXED: Re-disabled memaccess debugging tool, as it creates
           a symlink called "sh" which is a pretty bad
          idea from Broadcom. (RT-AC86U, RT-AX88U)


384.11 (8-May-2019)
  - NEW: Added DNS Privacy feature, with support for
         DNS-over-TLS (also known as DoT).
         You can configure it on the WAN -> Internet Connection
         page.  You can manually add your own servers, or chose
         one (or a few) from the preset list.  (themiron)
  - NEW: NTP daemon on the router, to allow your LAN clients to
         synchronize their clocks with it.
  - NEW: Option to intercept NTP requests from clients, and
         redirect them to the router's own NTP daemon.
  - NEW: Added service-event-end custom script, executed at the
         end of an rc service call.  Receives the same arguments
         as service-event, but is a non-blocking script.
  - NEW: Added sqlite3 CLI command, to allow script authors to
         create/manage their own sqlite3 database
  - UPDATED: RT-AX88U to 384_5951 GPL.
  - UPDATED: Other models to 384_45713 GPL (RT-AC87U, RT-AC3200
             and RT-AC5300 still using 384_45149 binary blobs)
  - UPDATED: Nano 4.0.
  - UPDATED: Curl 7.64.1.
  - UPDATED: Dropbear 2019.78.
  - CHANGED: Replaced the custom ntpclient with a proper ntpd
             implementation, for reduced memory usage and
             increased accuracy.
  - CHANGED: Made the secondary NTP server configurable through the
             webui.  Note that ntpd will use both servers, so clear
             the second server if there is one and you don't want
             to use it.
  - CHANGED: Re-designed firmware upgrade page, moving the schedule
             option to that page, and removed support for the Beta
             channel.
  - CHANGED: Removed popup messages showing on the DDNS page when
             a service state change was detected.  Report it within
             the page instead.
  - CHANGED: Report firmware version within the new firmware
             notification popup that appears at the top of the webui.
  - CHANGED: Moved LED control (formerly known as Stealth Mode) to
             the System page.
  - CHANGED: Do not restart whole network whenever changing an IP
             reservation on the Networkmap card.
  - CHANGED: Allow URLs up to 64 chars long on the URL filter.
  - CHANGED: pre-mount user script now receives the filesystem
             as second argument.
  - CHANGED: Moved various DNS-related settings from the DHCP page
             to a more appropriate location on the WAN page.
  - CHANGED: OpenSSL default dir moved to /etc/ssl/.  Allows
             programs to automatically locate the CA bundle
             without requiring explicit configuration.
  - CHANGED: Optimized service restarts generated by the
             System page.
  - CHANGED: Replaced Network Analysis and Netstat pages (under
             Network Tools) with new versions based on Asus's
             Netool daemon (RT-AC86U, RT-AX88U)
  - FIXED: Reboot scheduler would sometime get stuck, or corrupt
           plugged USB drives.  Now doing a more thorough
           shutdown of services, should hopefully make it
           more reliable.
  - FIXED: CVE-2019-1543 issue with Chacha20-poly1305 in
           OpenSSL 1.1 (themiron)
  - FIXED: Client count on the Sysinfo page was missing
           Guest clients
  - FIXED: Miniupnpd sometimes sending ssdp notifies to
           the wrong interface (themiron)
  - FIXED: udpxy not working when using the Movistar
           IPTV profile on RT-AC86U and RT-AX88U.


384.10_2 (3-Apr-2019)
  - CHANGED: Increased OpenVPN interface queue length from 100
             to 1000 bytes, to reduce the amount of dropped
             packets if router can't keep up.
  - CHANGED: Updated CA bundle to January 23rd version
  - FIXED: Moviestar VLAN routes weren't properly configured
           (broken quagga configuration)
  - FIXED: Layout issues on the Wireless Log page for some
           models
  - FIXED: Missing tooltip content for the new local DNS
           resolution setting on the Tweak page
  - FIXED: FAQ URL on Bandwidth Monitor points to a non-existing
           page on Asus's servers (point to old page for now)
  - FIXED: OpenVPN CA would be overwritten if there was no
           server key or cert present - only generate them
           if all three are missing.
  - FIXED: Bandwidth Limiter not working properly in some
           cases, as it failed to disable hardware acceleration


384.10 (24-March-2019)
  - NEW: Added OpenSSL 1.1.1b in parallel to 1.0.2.  Some services
         like AiCloud are still linked against 1.0.2 because they
         would require Asus to recompile them against 1.1.1.

         Main services that currently use OpenSSL 1.1.1:
         httpd (webui), OpenVPN, wget, net-snmp, Tor,
         Strongswan (IPSEC server), inadyn, vsftpd, avahi.

         Models that lack AES acceleration will prioritize the use
         of CHACHA20 over AES-256-GCM, for a small performance
         improvement (for instance with the webui).

         Note that OpenVPN 2.4.7's support is still limited.
         TLS 1.3 is supported, but CHACHA20 support is
         only expected with OpenVPN 2.5.0.

         The 1.0.2 userspace tool is still named "openssl", while
         the 1.1.x version is named "openssl11".

  - NEW: Updated RT-AX88U to GPL 384_5640.
  - NEW: Implemented lcp-ident option in PPP (required by some ISPs)
         (Themiron).
  - NEW: Added NFSv2 support to HND models.
  - NEW: You can now choose between having your router do internal
         DNS queries locally (through dnsmasq) or with your WAN
         configured DNS (like stock firmware).  This does not
         affect DNS lookups from your clients, only those made
         by the router itself.  The option is under Tools ->
         Other Settings.  (Themiron)
  - CHANGED: Some firmware cleanups to regain flash space (for
             use with the parallel OpenSSL 1.1.x install)
             (RMerlin, Themiron)
  - CHANGED: Updated curl to 7.64.0.
  - CHANGED: Updated OpenVPN to 2.4.7.
  - CHANGED: Updated Tor to 0.3.5.8.
  - CHANGED: Updated strongswan to 5.7.2.
  - CHANGED: Updated OpenSSL 1.0.x to 1.0.2r.
  - CHANGED: Updated dnsmasq to 2.80-44-g608aa9f (Themiron)
  - CHANGED: Re-worked the Classification page.  New design
             is much faster, allows filtering, and shows
             additional info when hovering on a field.  Thanks
             to FreshJr for giving me the motivation to
             spend more time on it.
  - CHANGED: Strongswan is no longer compiled 64-bit
             on HND, allowing it to use a shared openssl library
             instead of a static one.  This should significantly
             reduce the memory and flash usage of Strongswan.
             (Themiron)
  - CHANGED: Reworked DNS WAN probe implementation (Themiron)
  - FIXED: IPSEC log display wasn't properly formatted (showed
                 entirely on a single line)
  - FIXED: Compatibility issues between recent Tuxera NTFS driver
           and Samba
  - FIXED: NFSv2 support
  - FIXED: PPP host-uniq support (Themiron)
  - FIXED: AiCloud not working on the RT-AX88U
  - FIXED: OpenVPN key/certs would sometime end up in nvram in
           addition to in /jffs
  - FIXED: Couldn't remove an existing OpenVPN key/cert by
           clearing the field on the webui
  - FIXED: Resetting OpenVPN client to Default values wasn't
           removing any existing Extra CA certificate
  - REMOVED: Beceem Wimax driver.  This is deprecated, and was
             already removed from the HND models.  This allows
             to reclaim close to 2 MB of flash space.
  - REMOVED: CFB and OFB ciphers from OpenVPN client


384.9 (2-Feb-2019)
  - NEW: Temporarily reorganized code in separate branches, to handle
         Asus's currently scattered firmware source code releases.
         The GPL situation for this release is as follow:
     o RT-AX88U: Merged GPL 384_5329
     o Other models: Merged GPL 384_45149.
     o Special binary blobs provided by Asus for the RT-AC87U
       and RT-AC3200 (compatible with 384_45149).

  - NEW: Added NFS client support (V2 and V3) to the
         RT-AC86U and RT-AX88U (already present in older models)
  - NEW: Report the number of spatial streams and the PHY type
         used by wireless clients for models supporting it
  - NEW: Display tracked connections on the QoS Stats page (now
         relabeled "Classification").
         Fields can be sorted by clicking on the column headers.
         Thanks to FreshJr for his help in deciphering the packet
         mark values.

  - NEW: Implemented ipsec.postconf and strongswan.postconf scripts.
  - KNOWN ISSUE: dcd process crashing on RT-AC86U (bug in Trend
                 Micro's code, outside of my control).
  - KNOWN ISSUE: IPv6s on Tracked Connections have their last
                 two bytes set to 00 (bug in Trend Micro's
                 code truncating the last two bytes).
  - KNOWN ISSUE: No IPS events logged (bug in Asus's code,
                 IPS should work, just fails to log hits)
  - KNOWN ISSUE: Networkmap listing may be unreliable.
                 (Bug in Asus's code)
  - KNOWN ISSUE: Users failing to read changelogs will
                 probably complain about the above issues.
                 (Outside of my control).
  - CHANGED: Updated wget to 1.20.
  - CHANGED: Updated nano to 3.2.
  - CHANGED: Updated curl to 7.62.0.
  - CHANGED: Updated Chart.js to 2.7.3.
  - CHANGED: Updated dnsmasq to 2.80-32-g28cfe36 (themiron)
  - CHANGED: Optimized some JS files to reduce their size
  - CHANGED: OpenVPN clients can now accept CNs up to 255 chars
             when using it to validate the certificate.
  - CHANGED: No longer reset the OpenVPN client's description,
             policy mode and existing rules when uploading an
             .ovpn config file.
  - CHANGED: No longer accept any server-provided route
             when OpenVPN client set to Policy (Strict).
  - CHANGED: Clients bound to DNSFilter rules will no longer
             bypass it by using DoT.  DNSFilter servers that
             support DoT (like Quad9) will only allow filtered
             clients to use that server
  - FIXED: Firmware update checks would not run at boot time
           on the RT-AX88U.
  - FIXED: Name resolution issues for /etc/hosts entries on
           HND models (themiron)
  - FIXED: Syslog not properly copied to JFFS on reboot
           (John Bacho)
  - FIXED: Volumes not properly unmounted on HND platform
           (John Bacho)
  - FIXED: Added missing TEE Netfilter target on the RT-AC86U
  - FIXED: SSH brute force protection didn't work in Dual WAN
           load balancing mode.
  - FIXED: httpd crashes on RT-AC86U (themiron)
  - FIXED: DNSFilter clients could use a different nameserver
           when using an IPv6 connection
  - FIXED: USB disk idle config changes not applying without a
           reboot.
  - FIXED: "Strict" DNS mode wasn't working properly with OpenVPN
           clients
  - FIXED: Cannot upload JFFS backup on HND models


384.8_2 (8-Dec-2018)
  - CHANGED: Updated miniupnpd to 20181205.
  - CHANGED: Push LAN domain to OpenVPN clients as DNS suffix
             for the connection.
  - FIXED: Cannot save custom settings on OpenVPN server page
           on non-HND models.
  - FIXED: Some webui pages fail to load properly in French
  - FIXED: dnsmasq fails to start when certain options are
           configured (themiron)
  - FIXED: Non-functionnal Show Password option on OpenVPN/PPTP
           server page for RT-AX88U (removed)
  - FIXED: Persistent SSL cert was wiped at boot time in
           some specific scenarios.


384.8 (2-Dec-2018)
  - NOTE: Asus has put the RT-AC56U on their End of Life
          list, meaning no further firmware releases from
          them.  Since it's impossible for me to support
          models without matching GPL releases from Asus,
          I also have to retire the RT-AC56U.  384.6 is
          the final release for that model.

  - NOTE: The RT-AC3200 and RT-AC87U are not supported by this
          release, Asus hasn't released any updated code yet for
          these models.

  - NEW: Added RT-AX88U support (based on GPL 384_4736).
  - NEW: Merged with GPL + binary blobs from 384_32799 (all
         supported models except RT-AX88U)
  - NEW: Add LZ4 V2 option to OpenVPN compression
         (more effective at handling already compressed
         data)
  - NEW: Added "extend" support to SNMP.
 - NEW: Added CleanBrowsing to DNSFilter supported services.
  - NEW: Webui HTTP LAN port can now be changed from the default 80.
  - NEW: Added support for the Netfilter TEE target.
  - CHANGED: Removed watchdog from OpenVPN clients, to avoid
             conflicting with more advanced configurations.
  - CHANGED: Vsftpd TLS mode will now reuse the web server
             certificate (including any Let's Encrypt generated
             one).
  - CHANGED: SSL crypto/cipher hardening for httpd (themiron)
  - CHANGED: Syslog will now ignore bwdpi debug output (themiron)
  - CHANGED: Reworked Wireless Log page, adding a new button to
             view low-level details (what stock firmware shows
             on its Wireless Log page), and removed redundant
             option to display DFS channel details.
  - CHANGED: Update dnsmasq to 2.80-11-g59e4703 (themiron)
  - CHANGED: Updated nettle to 3.4
  - CHANGED: Updated net-snmp to 5.8
  - CHANGED: Updated openssl to 1.0.2q
  - CHANGED: Migrated /jffs/ssl/* content to /jffs/.cert (to
             share the same folder used by Asus stock)
  - CHANGED: Re-enabled WTFast on non-HND models (curl-related
             crash has been fixed).  This is still untested.
  - CHANGED: Updated CA bundle to October 17th 2018 version.
  - CHANGED: Support search domains pushed by a remote OpenVPN
             server
  - FIXED: UOPNP port forwarding not working in CGNAT/double NAT
           scenario even if proper ports were forwarded upstream.
  - FIXED: Pages based on table.js (like the port trigger one)
           would fail to work properly under Firefox
           (Michael Ziminsky)
  - FIXED: Dnsmasq issues when running in non-router mode
           (John Bacho)
  - FIXED: Routing issues when in non-router mode (John Bacho)
  - FIXED: Bug in curl that could cause some applications to
           crash on non-HND models
  - FIXED: IFTTT failing to start on non-HND models (caused by
           curl issue).
  - FIXED: Webui could complain about port 8080 being reserved for
           http WAN port (which is no longer supported)
  - FIXED: Cannot change image for device with a vendor name
           containing an apostrophe (like Micro-Star int'l)
           (Asus bug)
  - FIXED: OpenVPN client download was capped by Adaptive QOS
           upload limit (fix devised by FreshJR)
  - FIXED: OpenVPN custom config might be lost after a reboot
           on the RT-AC86U.


384.7_2 (21-Oct-2018)
  - FIXED: Namecheap DDNS service not working
  - FIXED: CVE-2018-15599 security issue in Dropbear
  - FIXED: Potential buffer overrun in httpd


384.7 (7-Oct-2018)
  - NOTE: The RT-AC3200 and RT-AC56U are not supported by this
          release, Asus hasn't released any updated code yet for
          these models.

  - NOTE: Important changes to DDNS, please read below.

  - NOTE: Important changes to DNSFilter, please read below.

  - NEW: Merged with GPL 384_21152.
  - NEW: Merged RT-AC87U binary blobs + SDK from 382_50702.
  - NEW: Replaced old ez-ipupdate DDNS client with In-a-Dyn.
         A plugin was developed to fully support Asus's DDNS
         service.
         Custom services can now be configured through ddns-start,
         inadyn.conf, inadyn.conf.add or inadyn.postconf.  See the
         In-a-Dyn documentation as many custom services can be
         defined for it.
  - NEW: Added support for freedns.afraid.org DDNS service to webui.
  - NEW: Added option to retrieve WAN IP from either the local
         interface (like before) or through a remote server
         (which works through double NAT) for DDNS.
  - NEW: Display DFS channel info on Wireless Log page.
  - NEW: Added option to disable checks on unsigned DNSSEC replies.
         Disabling these will speed up lookups, but it will also
         remove part of the security benefits of DNSSEC, so it
         should not be used unless you have a very specific reason
         to do so.
  - NEW: Added Quad9 to DNSFilter supported services.
  - CHANGED: Updated curl to 7.61.1.
  - CHANGED: Updated wget to 1.19.5.
  - CHANGED: Updated openssl to 1.0.2p.
  - CHANGED: Updated dnsmasq to v2.80test8 (themiron).
  - CHANGED: Updated nano to 3.1.
  - CHANGED: All DDNS services now use HTTPS.
  - CHANGED: Replaced Google Domains DDNS script with In-a-Dyn's own
             plugin.
  - CHANGED: Moved DNSFilter to the LAN section, to make it clear
             that it's unrelated to Trend Micro's engine.
  - CHANGED: Report hostname and IP on Wireless Log page if the
             info is missing from dnsmasq but available from
             networkmap.
  - FIXED: Invalid dnsmasq config when setting DNSFilter to Router
           mode and having IPv6 enabled (themiron).
  - FIXED: dnsmasq crashing on RT-AC86U with IPv6 Stateful mode
           (themiron).
  - FIXED: client table would be shown twice on the VPN Status
           page if the only connections to an OVPN server
           were invalid clients (like a port scanner)
  - FIXED: DDNS forced updates after "x" days wouldn't be
           initiated.
  - FIXED: CERT VU#598349 vulnerability (DHCP client could
           claim the special "wpad" hostname)
  - REMOVED: Ez-ipupdate DDNS client (replaced with In-a-Dyn).
             Update your scripts if you were relying on it.
  - REMOVED: Norton Safe DNSFilter services (being discontinued
             by Symantec in November).  Configured clients will
             be automatically migrated to OpenDNS Family - make
             sure to edit your DNSFIlter settings if you desire
             to use a different service.


384.6 (25-July-2018)
   - NOTE: The RT-AC87U is not supported in this release, as
           Asus hasn't released any updated code for that model.
   - NEW: Merged with GPL 384_21045/382_50624.
   - NEW: Added support for the "-p" option to netstat.
   - NEW: Added setting to enable DNS rebind protection, on the
          DHCP page.  This works by rejecting upstream server
          responses that would point at a private IP.
   - CHANGED: Updated nano to 2.9.8
   - CHANGED: Updated curl to 7.60.0 (contains security fixes)
   - CHANGED: Allow selecting text (for copy/paste operations)
              on AiProtection pages.
   - CHANGED: Added AES-*-GCM ciphers to the OpenVPN legacy
              ciphers (so they can be explicitely used without
              using NCP).
   - CHANGED: Updated dnsmasq to 2.80test2-17-g51e4eee (themiron)
   - CHANGED: Since dnsmasq 2.80, dnsmasq now ensures that unsigned
              DNS replies received with DNSSEC enabled are legitimate.
              If your upstream DNS doesn't support DNSSEC, this means
              all replies from signed zones will be considered
              invalid.  Make sure you only enable DNSSEC if your
              upstream DNS servers do support it.  This behaviour is
              a bit slower, but far more secure than the old default.
   - CHANGED: Network Tools -> Netstat output also report program/PID
   - CHANGED: Updated CA bundle to June 20th version.
   - FIXED: IPv6-related issues on non-HND platform (themiron)
   - FIXED: Couldn't log on WTFast if accessing the router
            webui over https.
   - FIXED: USB modem support code failing to properly pass
            parameters to the kernel module (themiron)
   - REMOVED: WTFast support for RT-AC88U/RT-AC3100/RT-AC5300,
              as it's incompatible with recent versions of
              curl (and has been broken for quite some time).
              Not gonna revert back to a 7 years old curl
              version just for wtfast.


384.5 (13-May-2018)
   - NEW: Merged withh GPL 384_20648
   - NEW: Merged RT-AC68U, RT-AC5300 binary blobs from 384_20648
   - NEW: Merged RT-AC86U SDK and binary blobs from 384_20648
   - NEW: service-event script, executed before any service
           call is made.  First argument is the event (typically
           stop, start or restart), second argument is the target
           (wireless, httpd, etc...).
           Note that this script will block the execution of
           the event until it returns.
   - NEW: Added USB HID modules (for use with devices such
          as UPS)
   - NEW: Added ip6tables-save command.
   - CHANGED: Updated OpenVPN to 2.4.6.
   - CHANGED: Updated Dropbear to 2018.76.
   - CHANGED: Updated Openssl to 1.0.2o.
   - CHANGED: Updated miniupnpd to version 2.1 (20180508).
   - CHANGED: Updated nano to 2.9.5.
   - CHANGED: Moved RT-AC86U to the same Busybox version (1.25.1)
              as other models.
   - CHANGED: Revised OpenVPN server options:
              o Removed "TLS Reneg time" (rarely used, can manually
                be set as a custom option)
              o Removed "Server Poll" (which didn't work
                properly), and reimplemented watchdog service,
                hardcoded to 2 mins frequency.
              o Removed "Push LAN" and "Redirect Gateway",
                replaced with new Client Access setting
              o Removed Firewall setting (firewall rules are now
                always created, and the broken External mode
                was fixed and integrated into the new Client
                Access setting).  You can now use the postconf
                script to override it.
              o Removed option to respond to DNS queries - enabling
                the option to Push DNS will also handle it
              o Added new Client Access setting to select between
                three types of access: LAN only, WAN only (will
                block access to the LAN, including the router
                itself) and LAN + WAN.
              o Keys and certificates can now be up to 7999
                characters long.

   - CHANGED: Revised OpenVPN client options:
              o Reorganized settings into groups
              o Removed "Poll Interval" (which didn't work
                properly), and reimplemented watchdog service,
                with a hardcoded frequency of 2 mins.
              o Removed Firewall setting (firewall rules are now
                always created).  You can now use the postconf
                script to override it.
              o Modified behaviour of Connection Retry.  Instead
                of taking a value in seconds that only affected
                resolution failure, it now takes a number of
                attempts, and affects connection failures.
                Resolution failures will now retry for an infinite
                period of time (the default OpenVPN value).
              o Added "refresh" link which can be clicked to
                re-query the public IP endpoint of the tunnel
              o Keys and certificates can now be up to 7999
                characters long.

   - CHANGED: Removed option to resolve names on the
              Log -> Connections page.
              That functionality was added to the
              Network Tools -> Netstat page instead.
   - CHANGED: Re-designed Log -> Connections page into a table
              with sortable fields - click on a column header to
              sort on that field.
   - CHANGED: From now on, setting the router to act as a master
              browser or a WINS server will also require you to
              enable sharing.  This will ensure that users understand
              that enabling either of these settings requires disk
              sharing to also be enabled (which it was already
              silently doing before).
   - CHANGED: Moved "Beta firmware" option to the Tools -> Other
              Settings page
   - CHANGED: Improved layout of the Firmware Update page
   - CHANGED: WPAD behaviour (sending a carriage return on
              DHCP option 252) can now be controlled in the
              Tweaks section.
   - CHANGED: Blocking custom scripts such as service-event
              and pre-mount will now wait a maximum of 120
              seconds before resuming normal operations, to
              prevent accidental lockouts.
   - CHANGED: Autofill start/end time for DST when selecting
              a timezone (LostFreq)
   - FIXED: Some dnsmasq issues related to DNSSEC were fixed,
            including CVE-2017-15107. (backported from
            dnsmasq 2.79 by John Bacho)
   - FIXED: Restoring an OpenVPN instance to default values
            would fail to disable its Start with WAN setting.
   - FIXED: Hardware authentication failure for the RT-AC3100
            and RT-AC5300.
   - FIXED: Minidlna web status page could no longer be enabled.
   - FIXED: CVE-2017-9022, CVE-2017-9023 and CVE-2017-11185 in
            Strongswan (odkrys)
   - FIXED: Various issues with download traffic in Traditional
            QoS (Cédric Dufour)
   - FIXED: TCP timeout values couldn't be changed on the
            Tools -> Other Settings page.
   - FIXED: Security issue related to webui logging in (Asus bug)


384.4_2 (24-Mar-2018)
   - CHANGED: Added visual warning when manually enabling webui
              access on WAN.  Doing so carries serious potential
              security risks, as Asuswrt's web server code should
              not be considered hardened enough for this.
   - FIXED: Security issue in httpd (CVE-2018-8879).
   - FIXED: Potential security issue in httpd related to QiS.
   - FIXED: Minor webui issue in the QoS overhead menu.


384.4 (16-Mar-2018)
   - NEW: Merged with GPL 384_20379 (with some binary components
          from 382_50010 and 384_20308 depending on models)
   - NEW: Added support for the RT-AC5300.
   - NEW: Added support for the RT-AC87U.
   - NEW: Added IPSEC support to the RT-AC86U.
   - NEW: Support the new Entware 64-bit repo on the RT-AC86U.
          To switch to the new repository, re-run the
          entware-setup.sh script.  You will need to reinstall
          your apps (your old config files are backed up on
          your USB disk).
   - CHANGED: Tightened security around some config files.
   - CHANGED: Allow guest networks settings for AP isolation
              and SSID broadcast to be set separately from
              their parent interface (John Bacho)
   - CHANGED: Samba protocol support can now be set to
              SMBv1, SMBv2, or SMBv1 + SMBv2 (the new default).
              This will result in a performance drop on all
              models but the RT-AC86U, but will be more secure.
              Ideally, people should change it to SMBv2 only,
              and then reboot all their client devices to start
              using only the new protocol.
   - CHANGED: Re-added some of the logging sd-idle used to do
              in 380.xx.
   - CHANGED: Switched to the new Entware repo for armv7 models.
              To upgrade, run the following commands TWICE:

              opkg update; opkg upgrade

   - FIXED: Resetting an OpenVPN client to default settings
            might revert back after a reboot.
   - FIXED: log flood from lldpd about "unable to send packet
            on real device" (moved to debug level)
   - FIXED: Potential racing condition that could lead to two
            instances of miniupnpd running at boot time.
   - FIXED: Single-char hostnames were rejected by DHCP static
            leasees page. (theMIROn)
   - FIXED: AiCloud could sometime generate a new SSL certificate
            that would overwrite the one stored in jffs.  Now,
            AiCloud can also use the same one uploaded by the
            user for the main webui, or the Let's Encrypt one.
   - REMOVED: Telnet server.  Please use SSH for console-based
              management.
   - REMOVED: SNMP support on the RT-AC86U (incompatible)
   - REMOVED: Merlin NAT loopback mode (was increasingly
              problematic as the firmware firewall handling became
              more complex)


384.3 (14-Feb-2018)
   - NOTE: To reduce confusion following the version
           bump to 384, the current Github repository
           was renamed from asuswrt-merlin.382 to
           asuswrt-merlin.ng (for New Generation).
           It's recommended that you update your
           local repository if you're a developer,
           for example by running:

              git remote set-url origin \
                 git@github.com:RMerl/asuswrt-merlin.ng.git

   - NOTE: AiMesh is currently not supported.  Feasability of
           supporting it is still under evaluation.
   - NEW: Merged with GPL 384_10007
   - NEW: Added support for RT-AC3200 (merged
          SDK 7.x-main + binary blobs from 382_19466).
   - NEW: nano can now be configured through /jffs/configs/nanorc
   - CHANGED: Allow up to 5 OpenVPN clients on RT-AC3200.
   - CHANGED: Updated nano to 2.9.3.
   - FIXED: Some routers coming from 380.xx would incorrectly
            report a new firmware available at boot time.
   - FIXED: Some broken clients (like Samsung TVs) try to use
            reserved hostnames - ignore these.  (theMIRon)
   - FIXED: Added missing IPv6 local hostnames (theMIRon)
   - FIXED: Issues withh DNS & broadcast relay for pptp
            clients (theMIRon)
   - FIXED: Fixed CVE-2018-5721 in httpd (Merlin & theMIROn)
   - FIXED: helper.js wasn't properly handling parentheses
            (John9527)
   - FIXED: NAT acceleration of PPPoE for some models (fix
            backported from 382_50010)
   - FIXED: Networkmap-related issues on some models (missing
            tx/rx rate and such).
   - FIXED: ipset could cause the router to crash on the HND
            platform (john9527)
   - FIXED: Network Service Filter wasn't working when in
            Blacklist mode.
   - FIXED: Repeater mode (backport from 384_20287)


382.2 Beta (17-Jan-2018)
   - NOTE: Due to various issues with GPL 382_18991, the 382.2
           release is being dropped, and work is moving on to the
           next version.  382.2 beta releases remain available
           for those who still wish to use it (especially RT-AC56U
           users for whom there is no ETA as to when Asus will
           release the next GPL for that particular model.)
           Known issues include lack of PPPoE HW acceleration and
           Adaptive QoS sometimes failing to start at boot among
           others.

   - NOTE: The official IRC channel has moved to
           Freenode (#asuswrt).

   - NEW: Merged with GPL 382_18991.
          Most notable changes (will vary between models):
            - Added IPSec VPN server
            - Added IFTTT and Alexa support
            - Let's Encrypt support (DDNS page)
            - Better support for some longer settings (RT-AC86U)
   - NEW: Merged HND SDK + binary components from 382_18848
          (RT-AC86U)
   - NEW: Added IPSec VPN status on the VPNStatus page.
   - NEW: Added support for RT-AC56U and RT-AC68U
          (and all of its variants)
   - NEW: Enabled support for Let's Encrypt on RT-AC56U and
          RT-AC68U (in addition to RT-AC88U/3100)
   - CHANGED: Moved HTTPS cert management to the DDNS page (where
              Asus has put theirs, as Let's Encrypt is tied to
              the DDNS configuration)
   - CHANGED: Updated openssl to 1.0.2n.
   - CHANGED: Updated tor to 0.2.9.14.
   - CHANGED: Updated nano to 2.9.1.
   - CHANGED: Updated curl to 7.57.0.
   - CHANGED: Increased max length for OpenVPN custom settings from
              170 to 510 characters on RT-AC86U.
   - CHANGED: Updated miniupnod to Github snapshot 20171212.
   - CHANGED: OpenVPN firewall rules are now processed after the
              various security chains (access restriction, network
              service firewall, etc...), ensuring OVPN traffic no
              longer bypasses them.
   - FIXED: httpd crash on certain web pages if there are no Ethernet
            clients connected
   - FIXED: DNSFILTER rules would have priority over OPENVPN Client
            rules (when client has DNS set to Exclusive mode).
   - FIXED: traffic routing from the router itself would fail when
            restarting the firewall while using an ovpn client with
            policy rules in effect.
   - FIXED: Dashes were rejected when used in an OpenVPN policy
            client description.
   - REMOVED: Removed option to select between active and passive
              scan mode for a site survey (that code is now closed
              source and therefore that option can no longer be
              implemented).


382.1_2 (2-Dec-2017)
   - NEW: Added custom/add/postconf support for mcpd.conf (RT-AC86U)
   - CHANGED: Updated odhcp6c to latest upstream version
              (patch by theMIRon)
   - CHANGED: cifs and xt_set kernel modules will get automatically
              loaded as needed.
   - CHANGED: Updated openssl to 1.0.2m.
   - CHANGED: Updated libogg to 1.3.3 and libvorbis to 1.3.5.
   - CHANGED: Merged wireless components from GPL 382_18991 for
              RT-AC88U and RT-AC3100 (should in theory fix KRACK
              issue on these two models)
   - FIXED: allow IA_NA mode downgrade with forced IA_PD
            (for ISPs with broken IPv6 support)
            (patch by theMIRon)
   - FIXED: SSH brute force protection would break WAN
            connectivity (RT-AC86U)
   - FIXED: Wrong Trend Micro signature updater was used when
            compiling with FW update checker enabled.
   - FIXED: QoS Upload chart missing on PPPoE connections with
            Adaptive QoS enabled.
   - FIXED: client and vendor id fields on WAN page would fail
            to accept new values longer than 32 characters.
   - FIXED: The Desc field in the OpenVPN policy section would
            reject ":" if field contained a MAC address.
   - FIXED: Security issues CVE-2017-15275, CVE-2017-12163 and
            CVE-2017-12150 (backported to Samba 3.6 and 3.5)
   - FIXED: DHCP static lease list would refuse any change if
            the list of leases+hostnames was longer than 1000
            chars due to an HND platform limitation (RT-AC86U)


382.1 (12-Nov-2017)
   Asuswrt-Merlin 382 was rebuilt from a clean GPL codebase, as
   merging the new 382 GPL on top of the existing code proved too
   difficult.

   For simplicity, the following abbreviations are used below:
      AM380 = Asuswrt-Merlin 380.xxx
      AM382 = Asuswrt-Merlin 382.xxx
      Asus380 = Asus's 3.0.0.4.380_xxxx
      Asus382 = Asus's 3.0.0.4.382_xxxx

   AM382.1 is based on AM380.68_4 merged on top of a clean
   3.0.0.4.382_15098 GPL.

   At this time, only the RT-AC86U, RT-AC88U and RT-AC3100
   are supported by AM382.  Other models will gradually be
   moved to AM382 as Asus upgrade them to the new 382 code
   base (and GPL code becomes available for them).

   This changelog will focus on changes that happened between
   AM380.68 and AM382.1, or between Asus382_16466 and AM382.

   Also note that the primary download site was changed to
   Sourceforge, due to numerous issues with Mediafire.  Onedrive
   will be the official mirror to the SF.net download site.

   - NEW: Moved to Asus382 codebase.  Some of the most important
          changes between Asus380 and Asus382:
            - New Trend Micro DPI engine, with two-way IPS
            - New networkmap service (now closed source)
            - New OpenVPN implementation (now closed source,
              not used by AM382)
            - Numerous security enhancements throughout the code

   - NEW: Merged with GPL 382_16466 (RT-AC86U).
   - NEW: Added support for the RT-AC86U and its Broadcom HND
          platform (HND SDK from GPL 382_18219).
          Note that IPTraffic is not supported by this model due to
          its newer Linux kernel.
   - NEW: Rewrote part of the OpenVPN implementation, as Asus's own
          is now closed source.  Asuswrt-Merlin's OpenVPN code will
          now be independent of Asus's.
   - NEW: Added support for inline CRLs when importing an ovpn file
   - NEW: Added support for fullcone NAT (RT-AC86U)
   - NEW: Added WiFi Radar (Broadcom's Visualization app) in the
          Wireless section.  You must enable data collection on
          its Configuration page for all charts to work properly.
          (RT-AC86U)
   - NEW: Added option to disable the Asus NAT tunnel service under
          Other Settings -> Tweak.  Not quite sure what this
          partly closed source service is for, but it eats a
          fair amount of CPU and RAM.
   - NEW: Option on OpenVPN Server page to quickly choose
          between pushing LAN or LAN + Internet access (ported
          from Asus382)
   - NEW: Option to select the bitsize to use (1024 or 2048) when
          automatically generating the OpenVPN server key/certs
          (ported from Asus382)
   - CHANGED: Updated wget to 1.19.2 (fixing connectivity to some
              TLS 1.2 servers)
   - CHANGED: SSH host keys are now stored in /jffs/ssl/ rather
              than nvram.
   - CHANGED: SMB2 is enabled by default on RT-AC86U (no performance
              penalty on that platform)
   - CHANGED: Moved UPnP Secure Mode setting from the Tweaks section
              to the WAN page, next to other UPnP settings.
   - CHANGED: Moved "Modify key and certs" link to its own dedicated
              row and made it a button for improved visibility
              (OpenVPN client & server pages)
   - CHANGED: Updated OpenVPN to 2.4.4.
   - CHANGED: The firmware version check behaviour was slightly
              changed.  The "Get Beta" checkbox will now check
              both the Beta and the Release channels for new
              version availability.  Automatic scheduled checks
              will still only check the Release channel.
   - CHANGED: Layout improvements to the SNMP, Login, and
              Operation Mode pages (patches by Alin Trăistaru)
   - CHANGED: Report both the local client IP as well as the
              public/visible IP on the OpenVPN client page once
              a client is connected (same info that was already
              available on the VPN Status page).
   - CHANGED: Moved Disk spindown settings to the System page,
              to match with Asus382 which now offers this feature.
   - REMOVED: Obsolete/exotic HMAC digests for OpenVPN servers (to
              match with Asus' own supported list)
   - REMOVED: "Custom" OpenVPN authentication mode (which probably
              nobody used or even understood).
