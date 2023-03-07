pkgname=duff
pkgver=0.5.2
pkgrel=1
pkgdesc="A command-line utility for quickly finding duplicates in a given set of files"
arch=('x86_64')
url="https://github.com/elmindreda/duff"
license=('custom')
depends=('glibc' 'sh')
source=("${pkgname}-${pkgver}.tar.gz::https://sourceforge.net/projects/duff/files/duff/0.5.2/${pkgname}-${pkgver}.tar.gz/download")
sha256sums=('SKIP')

build() {
  cd ${pkgname}-${pkgver}
  ./configure --prefix=/usr --mandir=/usr/share/man
  make
}

package() {
  cd ${pkgname}-${pkgver}
  make DESTDIR="$pkgdir" install
  install -D -m644 COPYING "$pkgdir"/usr/share/licenses/${pkgname}/COPYING
}
