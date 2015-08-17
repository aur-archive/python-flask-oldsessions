# $Id:$
# Maintainer: Antonio Rojas <arojas@archlinux.org>

pkgname=('python-flask-oldsessions' 'python2-flask-oldsessions')
pkgver=0.10
pkgrel=1
pkgdesc='Provides a session class that works like the one in Flask before 0.10'
url='https://github.com/mitsuhiko/flask-oldsessions'
arch=('any')
license=('custom:BSD')
makedepends=('python-setuptools' 'python2-setuptools')
source=("https://github.com/mitsuhiko/flask-oldsessions/archive/$pkgver.tar.gz")
sha256sums=('056e16cbe89187dc5c5fff019aa20c60daec32be2334848f4b813ce51e6701fb')

prepare() {
  cp -r "flask-oldsessions-$pkgver" "python-flask-oldsessions-$pkgver"
  cp -r "flask-oldsessions-$pkgver" "python2-flask-oldsessions-$pkgver"
}

build_python-flask-oldsessions() {
  cd "$pkgname-$pkgver"

  python setup.py build
}

build_python2-flask-oldsessions() {
  cd "$pkgname-$pkgver"

  python setup.py build
}

package_python-flask-oldsessions() {
  depends=('python-flask')
  cd "$pkgname-$pkgver"

  python setup.py install --prefix=/usr --root="$pkgdir" --optimize=1
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

package_python2-flask-oldsessions() {
  depends=('python2-flask')
  cd "$pkgname-$pkgver"

  python2 setup.py install --root="$pkgdir" --optimize=1
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

