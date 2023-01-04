# Maintainer: Felix Schindler <aut at felixschindler dot net>

_pkgname=git-sync
pkgname=${_pkgname}-git
pkgver=r56.8ced891
pkgrel=1
pkgdesc="Synchronize tracking repositories (master branch)"
arch=('any')
url="https://github.com/simonthum/git-sync"
license=('CC0')
depends=('git')
source=(git+https://github.com/simonthum/git-sync.git#branch=master)
sha256sums=('SKIP')
pkgver() {
  cd "${srcdir}/${_pkgname}"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  echo "nothing to build"
}

package() {
  cd "${srcdir}/${_pkgname}"

  install -D -m 755 git-sync "${pkgdir}/usr/bin/git-sync"
}
