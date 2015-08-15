# Maintainer: Federico Damián <federicodamians@gmail.com>
#
# PKGBUILD for Emerald Icon Theme
#

pkgname=emerald-icon-theme
pkgdesc="Clean and fresh icons theme. Based on Flattr (Nitrux OS) and Breeze (Plasma 5) icon themes."
pkgver=2.0
pkgrel=5
arch=('any')
url="http://vinceliuice.deviantart.com/art/Emerald-icons-theme-490755152"
license=('CC BY-NC-SA 4.0')
makedepends=('p7zip')
optdepends=()
source=('http://orig12.deviantart.net/4b5c/f/2015/122/b/2/emerald_icons_theme_by_vinceliuice-d846l3k.7z')
md5sums=('SKIP')

package() {

  install -d -m 755 "$pkgdir"/usr/share/icons/Emerald
  install -d -m 755 "$pkgdir"/usr/share/icons/Emerald-Dark
  install -d -m 755 "$pkgdir"/usr/share/icons/Emerald-Gray

  cd $srcdir/Emerald
  cp -r . "$pkgdir"/usr/share/icons/Emerald/
  cd $srcdir/Emerald-Dark
  cp -r . "$pkgdir"/usr/share/icons/Emerald-Dark/
  cd $srcdir/Emerald
  cp -r actions "$pkgdir"/usr/share/icons/Emerald-Gray/
  cd $srcdir/Emerald-Dark
  cp -r {animations,apps,status,index.theme} "$pkgdir"/usr/share/icons/Emerald-Gray
  sed -i 's/Emerald-Dark/Emerald-Gray/I' index.theme
}
