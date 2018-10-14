# Maintainer: Jurriaan Pruis <email@jurriaanpruis.nl>

pkgname=deconz
arch=('x86_64' 'armv6h' 'armv7h' 'aarch64')
pkgver=2.05.39
pkgrel=4
pkgdesc="A generic ZigBee monitoring and control tool"
url="http://www.dresden-elektronik.de"
license=('custom:"Copyright (c) dresden elektronik ingenieurtechnik GmbH"')
groups=()
depends=('hicolor-icon-theme'
         'libcap'
         'libpng'
         'qt5-base'
         'qt5-serialport'
         'qt5-websockets'
         'sqlite')
makedepends=('xz')
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source_x86_64=(https://www.dresden-elektronik.de/deconz/ubuntu/beta/$pkgname-dev-$pkgver.deb)
source_armv6h=(http://www.dresden-elektronik.de/rpi/deconz/beta/$pkgname-dev-$pkgver.deb)
source_armv7h=(http://www.dresden-elektronik.de/rpi/deconz/beta/$pkgname-dev-$pkgver.deb)
source_aarch64=(http://www.dresden-elektronik.de/rpi/deconz/beta/$pkgname-dev-$pkgver.deb)
noextract=()
sha256sums_x86_64=(SKIP)
sha256sums_armv6h=(SKIP)
sha256sums_armv7h=(SKIP)
sha256sums_armv7h=(aarch64)

package() {
  cd "${srcdir}"

  tar -xJf data.tar.xz -C "${pkgdir}"

  chown -R root:root "${pkgdir}"
  cp -rfv "${pkgdir}/lib" "${pkgdir}/usr"
  rm -rf "${pkgdir}/lib"

  # Remove group write permissions from all files/directories
  chmod -R g-w "${pkgdir}"
}
