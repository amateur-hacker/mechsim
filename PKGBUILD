pkgname=mechsim
pkgver=1.0
pkgrel=1
pkgdesc="CLI-based mechanical keyboard sound simulator"
arch=('x86_64' 'aarch64')
url="https://github.com/amateur-hacker/mechsim"
license=('MIT')
options=('!debug')

depends=(
  'json-c'
  'libpulse'
  'systemd-libs'
)

makedepends=(
  'gcc'
  'make'
  'pkgconf'
  'libevdev'
  'libinput'
  'libsndfile'
)

source=("$pkgname::git+$url.git")
sha256sums=('SKIP')

build() {
  cd "$srcdir/$pkgname"
  make PREFIX=/usr
}

package() {
  cd "$srcdir/$pkgname"
  make DESTDIR="$pkgdir" PREFIX=/usr install
}
