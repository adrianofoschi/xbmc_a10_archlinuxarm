XBMC_A10_ARCHLINUXARM
==========

ArchlinuxARM XBMC PKBUILDS for A10 devices (Cubieboard 1 etc..) with Video Acceleration enabled.



Native compilation/installation:

1) make and install sunxi-mali-fb-git,sunxi-mali-libump-git

#cd sunxi-mali-fb-git
#makepkg -si

NOTE: update mesa version in PKGBUILD
Go to line line #40 of PKGBUILD (package_sunxi-mali-fb-git provides section) and replace mesa=9.2.3 with the current ArchlinuxARM mesa version. This will resolve conficts between sunxi and mesa.

2) make and install cedarx-libs-git

#cd cedarx-libs-git
#makepkg -si

3) make and install xbmc a10 patched version

#cd xbmc-a10
#makepkg -si

NOTE: I suggest to enable ccache in /etc/makepkg.conf becouse the native compilation on Cubieboard takes about 2 hours.
If you want you can try cross-compilation from ArchlinuxARM wiki.
