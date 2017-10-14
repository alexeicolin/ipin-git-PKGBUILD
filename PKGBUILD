# Maintainer: Alexei Colin <ac at alexeicolin.com>

pkgname=ipin-git
pkgver=0.r0.g3ff0cd6
pkgrel=1
pkgdesc="Script to pin files or URLs into IPFS"
url='http://tasktools.org/projects/taskd.html'

source=("${pkgname}::git+https://github.com/alexeicolin/ipin.git")

sha256sums=('SKIP')

arch=('any')
makedepends=('git')
provides=('ipin')
conflicts=('ipin')

pkgver() {
    cd "${pkgname}"
    git describe --tags --long | sed 's/^v//;s/\([^-]*-g\)/r\1/;s/-/./g'
}

package() {
    cd "${srcdir}/${pkgname}"

    install -Dm755 ipin "${pkgdir}/usr/bin/ipin"
}
