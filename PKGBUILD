# Maintainer:  Devin Cofer <ranguvar{AT]archlinux[DOT}us>
# Contributor: Imanol Celaya <ilcra1989@gmail.com>

pkgname=openbsd-ksh
pkgver=5.2
pkgrel=0
pkgdesc="OpenBSD's ksh"
arch=('i686' 'x86_64')
url="http://deftly.net/openbsd-ksh"
license=('BSD')

depends=('bmake-mk-files')
depends=('bmake')

source=("http://deftly.net/openbsd-ksh-$pkgver.tar.gz")
sha256sums=('e3d518f67822a7201d40237b9897299cc04e74a450c3b558e46ee5c9ed2a444d')

build() {
  cd openbsd-ksh-5.2
  bmake -f Makefile
}
package() {
	install -Dm755 openbsd-ksh-5.2/ksh "$pkgdir"/bin/ksh
	install -Dm644 openbsd-ksh-5.2/ksh.1 "$pkgdir"/usr/share/man/man1/ksh
}
