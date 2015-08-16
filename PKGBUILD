# $Id: PKGBUILD 83713 2013-02-04 16:16:05Z spupykin $
# Maintainer: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Maintainer: Giovanni Scafora <linuxmania@gmail.com>

pkgname=ksniffer
pkgver=0.3.2
pkgrel=6
pkgdesc="A sniffing application for KDE"
arch=('i686' 'x86_64')
url="http://www.ksniffer.org"
license=('GPL2')
depends=('libpcap' 'kdelibs3')
source=(http://downloads.sourceforge.net/ksniffer/${pkgname}-${pkgver}.tar.bz2)
md5sums=('dee2cfc8b51d15857ee02382d2603a22')

build() {
  cd $srcdir/${pkgname}-${pkgver}
  source /etc/profile.d/kde3.sh
  source /etc/profile.d/qt3.sh
  ./configure --prefix=/opt/kde --without-arts
  make
}

package() {
  cd $srcdir/${pkgname}-${pkgver}
  make DESTDIR=$pkgdir install
}
