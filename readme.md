Asuswrt-Merlin 384/NG Changelog
===============================

384.19 (14-Aug-2020)
  - NOTE: Due to flash partitioning changes done by Asus, it is
          strongly recommended to make a backup of your JFFS
          partition before upgrading the RT-AC86U, and restoring
          that backup afterward.  If you run into issues,
          reformat your JFFS partition and reboot.
  - NOTE: The RT-AX56U build is not available for this release.

  - NEW: Added support for static routes for PPTP/L2TP VPN
         clients, on the Static Route page (themiron)
  - NEW: Added notification when JFFS free space drops
         below 3 MB.
  - UPDATED: Merged GPL 384_9354 for AX models.
  - UPDATED: Merged GPL 384_81992 for mainline models.
  - UPDATED: Merged SDK + binary blobs 384_9354 for RT-AX58U.
  - UPDATED: Merged SDK + binary blobs 384_9107 for RT_AX88U.
  - UPDATED: Merged binary blobs + SDK 384_81981 for RT_AC5300.
  - UPDATED: Merged binary blobs + SDK 384_81992 for RT-AC86U.
  - UPDATED: Merged bwdpi components from 385_20630 firmware
             image for RT-AC68U.
  - UPDATED: dnsmasq to 2.82-openssl (themiron)
  - CHANGED: Rewrote a large portion of the OpenVPN implementation,
             to make the code easier to maintain.  The new libovpn
             code is released under a GPL licence.  Functionality
             should largely remain the same.
  - CHANGED: Replaced updown-*.sh OpenVPN event handler scripts
             with binary libovpn functions. The new code does
             stricter validation of the configuration.
  - CHANGED: Enabling Client Config Dir (ccd) for an OpenVPN
             server in non-exclusive mode will no longer accept
             duplicate common names (to prevent issues with
             two clients trying to share the same settings).
             If you need such an unusual setup, you should
             enable "Username/Password auth only", which will
             make the common name become the username.  Or
             better, ensure that you have unique certificates
             for all of your users.
  - CHANGED: Removed the (undocumented) vpn_debug setting.  Debug
             logging will now only come from OpenVPN itself
             (configurable through the log verbosity setting).
  - CHANGED: Improved mechanism for providing an available
             mount point for addon API scripters (dave14305)
  - CHANGED: Harmonized the various SSL certificate modes with
             upstream.
             0-None - will be self-generated
             1-Imported - lets you upload your own (no longer
                           self generated unless you don't
                           upload one)
            2-Let's Encrypt (unchanged)
            Self-generated cert will be stored to /jffs/cert.tgz,
            just like upstream.
  - FIXED: Broken French webui on AX models (fixed with
           Asus's GPL update)
  - FIXED: Chacha20 wasn't prioritized for bcm675x models which
           lacked AES acceleration (RT-AX56U and RT-AX58U)
  - FIXED: ddns updates and OpenVPN instances might be launched
           twice at boot time if the initial ntp clock sync
           happened too fast.
  - FIXED: Enforced DNS and tQoS fix would be lost when the
           firewall gets restarted while an OpenVPN client
           is running.
  - FIXED: Various issues surrounding error state report
           when an OpenVPN client failed to start properly.
  - FIXED: WINS provided by an OpenVPN server weren't properly
           used.
  - FIXED: Some large DNS queries could fail when using DoT
           (patch backported from upstream)