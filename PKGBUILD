# Maintainer: Felix Yan <felixonmars@gmail.com>

pkgname=boinctui
pkgver=2.3.5
pkgrel=1
pkgdesc="Curses based fullscreen BOINC manager"
arch=('i686' 'x86_64')
url="http://boinctui.googlecode.com/"
license=('GPL')
depends=('expat' 'gcc-libs' 'gnutls')
makedepends=("cmake")
source=("http://sourceforge.net/projects/boinctui/files/${pkgname}_${pkgver}.tar.gz")

build() {
  cd $pkgname-$pkgver
  autoconf
  ./configure --prefix=/usr
  make 
}

package() {
  cd $pkgname-$pkgver
  make DESTDIR="$pkgdir" install
}

sha512sums=('c60ffeb69abeb013ff331c13d8737ea526641f7e8114562a9878ceeeeafa052f467a5ea15ae91cf7a47ea1d0fe69ed545c2b695c11e18207b14b423d59dcab34')
