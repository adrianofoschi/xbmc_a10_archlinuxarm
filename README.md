XBMC_A10_ARCHLINUXARM
==========

ArchlinuxARM XBMC PKBUILDS for A10 devices (Cubieboard 1 etc..) with Video Acceleration enabled.

##Installation (testing with mesa 9.2.3)

cd binaries

pacman -U libump-git-26.9971394-1-armv7h.pkg.tar.xz

pacman -U sunxi-mali-fb-git-26.9971394-1-armv7h.pkg.tar.xz

pacman -U cedarx-libs-git-20130909.b8f52d9-1-armv7h.pkg.tar.xz

pacman -U xbmc-a10-20130925.e7d9567-1-armv7h.pkg.tar.xz


##Native compilation/installation:

1) make and install sunxi-mali-fb-git,sunxi-mali-libump-git

cd sunxi-mali-fb-git

makepkg -si

NOTE: update mesa version in PKGBUILD
Go to line line #40 of PKGBUILD (package_sunxi-mali-fb-git provides section) and replace mesa=9.2.3 with the current ArchlinuxARM mesa version. This will resolve conficts between sunxi and mesa.

2) make and install cedarx-libs-git

cd cedarx-libs-git

makepkg -si

3) make and install xbmc a10 patched version

cd xbmc-a10

makepkg -si

NOTE: I suggest to enable ccache in /etc/makepkg.conf becouse the native compilation on Cubieboard takes about 2 hours.
If you want you can try cross-compilation from ArchlinuxARM wiki.
