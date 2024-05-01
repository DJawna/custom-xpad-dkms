# Maintainer: djawna@gmail.com
pkgname=custom-xpad
pkgver=0.4
pkgrel=1
epoch=
pkgdesc="This is a custom modofication of the xpad kernel module"
arch=('x86_64')
url="https://github.com/DJawna/custom-xpad-dkms"
license=('GPL')
groups=()
depends=(
	'dkms'
)
makedepends=(
	'git'
)
checkdepends=()
optdepends=()
provides=(
	'custom-xpad'
)
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("git+https://github.com/DJawna/xpad.git#commit=21b5c6d")
noextract=()
sha256sums=()
validpgpkeys=()

package() {
	cd "$pkgname-$pkgver"
	dkms install -m xpad -v 0.4
}
