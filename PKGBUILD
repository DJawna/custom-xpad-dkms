# Maintainer: djawna@gmail.com
pkgname=custom-xpad
pkgver=0.4
pkgrel=1
epoch=
pkgdesc=""
arch=()
url=""
license=('GPL')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
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
	sudo dkms install -m xpad -v 0.4
}
