# Maintainer: djawna@gmail.com
_pkgname=xpad
pkgname=custom-xpad-dkms
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
	'linux-headers'
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
source=("git+https://github.com/DJawna/xpad.git#commit=67beebb")
noextract=()
sha256sums=('SKIP')
validpgpkeys=()

package() {
	echo "* copying module into /usr/src..."
	install -dm755 "${pkgdir}/usr/src/${_pkgname}-${pkgver}"
	cp  -r "${srcdir}/$ ./xpad/* /usr/src/${_pkgname}-${pkgver}"
}
