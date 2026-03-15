# Maintainer: fft
# Contributor: foutrelis
# Contributor: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Stefan Husmann <stefan-husmann@t-online.de>

pkgname=mimetex
pkgver=1.76
_pkgver=1.75
pkgrel=3
pkgdesc='tex to gif converter'
arch=('x86_64')
url='http://www.forkosh.com/mimetex.html' #https://web.archive.org/web/20170606175051if_/http://www.forkosh.com/mimetex.zip
depends=('glibc')
license=('GPL-3.0-or-later')
source=("http://deb.debian.org/debian/pool/main/m/${pkgname}/${pkgname}_${pkgver}.orig.tar.gz")
b2sums=('ef295862d9587c68e62e894bdbc0278ab1b8169c75264bcdd7266ccd9b08af1b360b1ad04667ce149083141edc84c5ddeeef475b27d943950c478124bf67af95')

build() {
  cd "${pkgname}-${_pkgver}"
  gcc -DAA ${CFLAGS} ${LDFLAGS} mimetex.c gifsave.c -lm -std=gnu17 -o mimetex.cgi
}

package() {
  cd "${pkgname}-${_pkgver}"
  install -D -m0755 -t "${pkgdir}/usr/bin/" mimetex.cgi
}
