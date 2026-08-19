# Maintainer: NevPeth <nevillepeth at gmail dot com>
pkgname=meloville-git
_pkgname='meloville'
pkgver=1.0.0
pkgrel=1
pkgdesc="A modern music player and manager built in Qt6"
arch=('x86_64')
url="https://github.com/NevPeth/meloville"
license=('GPL-3.0-or-later')
options=(!debug)

depends=(
    'qt6-base'
    'qt6-declarative'
    'qt6-multimedia'
    'qt6-svg'
    'taglib'
    'libpulse'
)

makedepends=(
    'cmake'
    'pkgconf'
)

source=(
    "meloville-${pkgver}.tar.gz::https://github.com/NevPeth/meloville/archive/refs/tags/v${pkgver}.tar.gz"
)

sha256sums=('9fada7cf662cbcca78af2b2cba8b2e97deb0dd9611eae8ec031fa878c12b24f0')

build() {
    cmake -B build \
        -S "meloville-${pkgver}/src" \
        -DCMAKE_BUILD_TYPE=Release \
        -DCMAKE_INSTALL_PREFIX=/usr

    cmake --build build
}

package() {
    DESTDIR="$pkgdir" cmake --install build
}