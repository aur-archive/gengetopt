# Maintainer: Christian Hesse <mail@eworm.de>
# Contributor: andreas_baumann <abaumann@yahoo.com>
# Contributor: zhuqin <zhuqin83@gmail.com>

pkgname=gengetopt
pkgver=2.22.6
pkgrel=3
pkgdesc="A tool to write command line option parsing code for C programs."
arch=('i686' 'x86_64' 'arm' 'armv6h')
url="http://www.gnu.org/software/gengetopt/gengetopt.html"
license="GPL"
options=('!docs' '!makeflags')
source=(ftp://ftp.gnu.org/gnu/gengetopt/${pkgname}-${pkgver}.tar.gz{,.sig})
validpgpkeys=('D459FCC2041AC8FEF297D53EB4AA8C689E629EAC')

build() {
	cd ${srcdir}/${pkgname}-${pkgver}

	./configure --prefix=/usr
	make
}

package() {
	cd ${srcdir}/${pkgname}-${pkgver}

	make DESTDIR=${pkgdir} install
}

sha256sums=('30b05a88604d71ef2a42a2ef26cd26df242b41f5b011ad03083143a31d9b01f7'
            'SKIP')
