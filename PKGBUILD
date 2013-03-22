# Maintainer: Joni Lapilainen <joni.lapilainen@gmail.com>

pkgname=uboot-n900-tools
pkgver=20130322
pkgrel=1
pkgdesc="U-Boot tools for Nokia N900"
arch=('armv7h')
url="http://www.gitorious.org/u-boot-shr/u-boot/commits/pali"
license=('GPL')
groups=()
depends=('uboot-mkimage')
makedepends=()
provides=()
conflicts=()
replaces=()
backup=('etc/default/u-boot-update-bootmenu')
options=()
install=uboot-n900-tools.install
source=(
'u-boot-gen-combined'
'u-boot-update-bootmenu'
'u-boot-update-bootmenu.conf')
noextract=()
md5sums=()

package() {
  install -D -m 755 "$srcdir/u-boot-gen-combined" "$pkgdir/usr/bin/u-boot-gen-combined"
  install -D -m 755 "$srcdir/u-boot-update-bootmenu" "$pkgdir/usr/bin/u-boot-update-bootmenu"
  install -D -m 644 "$srcdir/u-boot-update-bootmenu.conf" "$pkgdir/etc/default/u-boot-update-bootmenu"
  ln -sr "$pkgdir/usr/bin/u-boot-gen-combined" "$pkgdir/usr/bin/uboot-combine"
  ln -sr "$pkgdir/usr/bin/u-boot-update-bootmenu" "$pkgdir/usr/bin/uboot-updatemenu"
}

# vim:set ts=2 sw=2 et:
