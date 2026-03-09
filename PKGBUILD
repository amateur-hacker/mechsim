pkgname=mechsim
pkgver=1.0
pkgrel=1
pkgdesc="CLI-based mechanical keyboard sound simulator"
arch=('x86_64')
url="https://github.com/amateur-hacker/mechsim"
license=('MIT')

depends=(
  'libevdev'
  'libinput'
  'libudev'
  'json-c'
  'libsndfile'
  'libpulse'
)

makedepends=(
  'gcc'
  'make'
  'pkgconf'
)

source=("$pkgname::git+https://github.com/amateur-hacker/mechsim.git")
sha256sums=('SKIP')

build() {
  cd "$srcdir/$pkgname"
  make PREFIX=/usr
}

package() {
  cd "$srcdir/$pkgname"
  make DESTDIR="$pkgdir" PREFIX=/usr install
}
