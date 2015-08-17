# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=shelltestrunner
pkgname=shelltestrunner
pkgver=0.9
pkgrel=2
pkgdesc="A tool for testing command-line programs."
url="http://hackage.haskell.org/package/${_hkgname}"
license=('GPL')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-filemanipcompat<0.16' 'haskell-hunit=1.2.2.1' 'haskell-cmdargs<0.2' 'haskell-directory=1.0.1.1' 'haskell-filepath=1.1.0.4' 'haskell-parsec=2.1.0.1' 'haskell-process=1.0.1.3' 'haskell-regex-tdfa<1.2' 'haskell-test-framework<0.4' 'haskell-test-framework-hunit<0.3' 'haskell-utf8-string<0.4')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/${_hkgname}/${pkgver}/${_hkgname}-${pkgver}.tar.gz)
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
}
md5sums=('30aa860c9c39337cae7ea5149ce1ed55')
