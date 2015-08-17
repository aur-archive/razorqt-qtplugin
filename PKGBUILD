# Maintainer: Dobroslaw Kijowski [dobo] <dobo90_at_gmail.com>

pkgname=razorqt-qtplugin
pkgver=0.1.2
pkgrel=1
pkgdesc='Icon theme changer for Razor-Qt'
url='https://github.com/dobo90/razorqt-qtplugin'
arch=(i686 x86_64)
license=(LGPL2)
depends=(qt4)
makedepends=(cmake)
install=${pkgname}.install
source=(https://github.com/dobo90/${pkgname}/archive/{$pkgver}.tar.gz)
md5sums=(ba0b9d0f5fa2e90542f56e2ead209e7e)

build() {
  cd ${srcdir}/${pkgname}-${pkgver}

  mkdir build
  cd build

  cmake ../ -DCMAKE_INSTALL_PREFIX=/usr -DQT_QMAKE_EXECUTABLE=qmake-qt4
  make
}

package() {
  cd ${srcdir}/${pkgname}-${pkgver}/build

  make DESTDIR=${pkgdir} install
}

