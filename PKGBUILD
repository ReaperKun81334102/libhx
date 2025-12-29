# Maintainer:
# Contributor: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Max Roder <maxroder@web.de>
# Contributor: Nathan Owe <ndowens.aur at gmail dot com>

pkgname=libhx
pkgver=5.2
pkgrel=1
pkgdesc='A library providing queue, tree, I/O and utility functions'
arch=(x86_64)
url='http://libhx.sourceforge.net/'
license=(GPL-3.0-only
         LGPL-3.0-only)
depends=(glibc)
makedepends=(git)
source=('https://inai.de/files/libhx/libHX-5.2.tar.zst')
sha256sums=('SKIP')

prepare() {
  cd libHX-5.2
  autoreconf -vi
}

build() {
  cd libHX-5.2
  ./configure --prefix=/usr
  make
}

package() {
  cd libHX-5.2
  make DESTDIR="$pkgdir" install
}
