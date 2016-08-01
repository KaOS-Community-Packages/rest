pkgname=rest
pkgver=0.8.0
_pkgver=0.8
pkgrel=1
pkgdesc="Library to access RESTful web services"
arch=('x86_64')
url="https://git.gnome.org/browse/librest"
license=('GPL2')
depends=('glib2' 'libxml2' 'libsoup')
makedepends=('gobject-introspection')
source=("http://download.gnome.org/sources/rest/${_pkgver}/${pkgname}-${pkgver}.tar.xz")
sha256sums=("e7b89b200c1417073aef739e8a27ff2ab578056c27796ec74f5886a5e0dff647")

build() {
  
  cd ${pkgname}-${pkgver}
  ./configure \
    --prefix=/usr \
    --sysconfdir=/etc \
    --without-gnome    
  
  make
}

package() {
  
  cd ${pkgname}-${pkgver}
  
  make DESTDIR="${pkgdir}" install
}
