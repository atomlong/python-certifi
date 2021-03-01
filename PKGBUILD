# Maintainer: Felix Yan <felixonmars@archlinux.org>
# Contributor: Massimiliano Torromeo <massimiliano.torromeo@gmail.com>
# Contributor: William J Bowman <bluephoenix47@gmail.com>

pkgname=python-certifi
pkgver=2020.12.05
pkgrel=1
pkgdesc="Python package for providing Mozilla's CA Bundle"
arch=(any)
url="https://pypi.python.org/pypi/certifi"
license=('GPL')
depends=('python')
makedepends=('python-setuptools')
source=(${pkgname}-${pkgver}.tar.gz::"https://github.com/certifi/python-certifi/archive/2020.12.05.tar.gz")
sha512sums=('e4a7059de92ef433feeb82cbf05435de328b8ea8e2a01a756481933599d82c24555188773b8bb15a35a33cfe0b51b7be97dc5b8665ad3640dd8464394bca9827')

build() {
  cd "$srcdir/${pkgname}-${pkgver}"
  python setup.py build
}

package() {
  cd "$srcdir/${pkgname}-${pkgver}"
  python setup.py install --skip-build -O1 --root="$pkgdir"
  install -m0644 -D "LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
