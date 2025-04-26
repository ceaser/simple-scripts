# Maintainer: Ceaser Larry <clarry@divergentlogic.com> -> https://github.com/ceaser/
pkgname=simple-scripts
pkgver=1.0.0
pkgrel=1
pkgdesc="Simple scripts I use"
arch=(x86_64)
url="https://github.com/ceaser/simple-scripts"
license=()
depends=()
makedepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
source=('git+https://github.com/ceaser/simple-scripts.git')
md5sums=('SKIP')

_gitname="todo"

pkgver() {
  cd "${srcdir}/github.com/${_gitname}/${_gitname}"
	printf "%s" "$(git describe --long --tags | sed 's/\([^-]*-\)g/r\1/;s/-/./g')"
}

prepare() {
  install -d "${srcdir}/github.com/${_gitname}"
  if [ -d "${srcdir}/github.com/${_gitname}/${_gitname}" ]; then
    rm -rf "${srcdir}/github.com/${_gitname}/${_gitname}"
  fi
  #mv $pkgname "${srcdir}/github.com/${_gitname}/${_gitname}"
  mv $pkgname "${srcdir}/github.com/${_gitname}/${_gitname}"
}

build() {
  cd "${srcdir}/github.com/${_gitname}/${_gitname}"
}

package() {
  cd "${srcdir}/github.com/${_gitname}/${_gitname}"
  install -Dm755 todo ${pkgdir}/usr/bin/todo
}
