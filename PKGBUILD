# $Id: pkgbuild-mode.el,v 1.23 2007/10/20 16:02:14 juergen Exp $
# Maintainer: Paul Blouët <paul@paulblouet.fr>
pkgname=upftii
pkgver=0.2.1
pkgrel=1
pkgdesc="ULTIMATE PRO FIGHTER TURBO II"
arch=('i686' 'x86_64')
url="https://github.com/Geogi/upftii"
license=('GPL3')
groups=()
depends=(sdl2 imagemagick)
makedepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://github.com/Geogi/upftii/releases/download/v$pkgver/$pkgname-$pkgver.tar.gz")
sha1sums=('1a0a82723e32e33299ce1376d17e7274d7108384')
noextract=()

build() {
  cd $srcdir/$pkgname-$pkgver

  ./configure --prefix=/usr
  make
}

package() {

  cd $srcdir/$pkgname-$pkgver

  make DESTDIR=$pkgdir install
}

# vim:set ts=2 sw=2 et:
