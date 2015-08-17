# Maintainer: Jonathan Liu <net147@gmail.com>
pkgname=python2-ipaddr
_realpkgname=ipaddr
pkgver=2.1.10
pkgrel=1
pkgdesc="An IPv4/IPv6 manipulation library in Python"
arch=('any')
url="http://code.google.com/p/ipaddr-py/"
license=('APACHE')
depends=('python2')
makedepends=('python2-distribute')
source=("http://ipaddr-py.googlecode.com/files/${_realpkgname}-${pkgver}.tar.gz")
md5sums=('f315ac829218e9735c5d772d59a3e0e7')

build() { 
  cd "${srcdir}/${_realpkgname}-${pkgver}"
  find "${srcdir}" -name '*.py' -exec sed -i -r "s|#!/usr/bin/python$|#!/usr/bin/python2|" {} +
  python2 setup.py build
}

package() {
  cd "${srcdir}/${_realpkgname}-${pkgver}"
  python2 setup.py install --root="${pkgdir}" -O1
}

# vim:set ts=2 sw=2 et:
