# Maintainer: Todd Partridge <https://github.com/Gen2ly/archpkgs>

pkgname=daeme-git
_pkgname=${pkgname%-*}
pkgver=0.80.1
pkgrel=1
pkgdesc="Basic, extremely-simple, scripts for Digital Audio Extraction (i.e. “ripping”)."
arch=("any")
url="https://github.com/Gen2ly/"$_pkgname"/"
license=("GPL2")
depends=("ripit")
makedepends=("git")
conflicts=("")
install=
source=("git://github.com/Gen2ly/"$_pkgname"")
md5sums=('SKIP')

pkgver() {
  cd $srcdir/$_pkgname
  git describe --long | sed -r 's/-([0-9,a-g,A-G]{7}.*)//' | sed 's/-/./'
}

package() {
  cd $srcdir/$_pkgname
  install -Dm755 $_pkgname   "$pkgdir"/usr/bin/$_pkgname
  install -Dm755 daefe       "$pkgdir"/usr/bin/daefe
  install -Dm644 license.txt "$pkgdir"/usr/share/licenses/$_pkgname/license.txt
}

# vim:set ts=2 sw=2 et:
