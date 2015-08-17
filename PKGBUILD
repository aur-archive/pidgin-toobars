# Contributor: JokerBoy <jokerboy at punctweb dot ro>

pkgname=pidgin-toobars
pkgver=1.14
pkgrel=1
pkgdesc="Pidgin plugin that adds a toolbar and status bar to the buddy list"
arch=('i686' 'x86_64')
url="http://vayurik.ru/wordpress/en/toobars/"
license=('GPL')
depends=('pidgin')
makedepends=('intltool')
options=('!libtool')
source=("http://vayurik.ru/wordpress/wp-content/uploads/toobars/${pkgver}/${pkgname}-${pkgver}.tar.gz")
md5sums=('0b9255902c10ec1b171329474bd69e82')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}
