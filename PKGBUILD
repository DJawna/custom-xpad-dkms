#aintainer: djawna@gmail.com
_pkgname=xpad-dja
pkgname=xpad-dja-dkms
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
	'xpad-dja-dkms'
)
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("git+https://github.com/DJawna/xpad.git#commit=b11f4fe")
noextract=()
sha256sums=('SKIP')
validpgpkeys=()

package() {
	echo "* installing /usr/src"
	install -dm644 "${pkgdir}/usr/src/${_pkgname}-${pkgver}"

	echo "* copying module into /usr/src..."
	cp -r "${srcdir}/xpad/"* "${pkgdir}/usr/src/${_pkgname}-${pkgver}/"
	
	echo "install blacklist '${srcdir}/xpad/modprobe.conf' -> '${pkgdir}/usr/src/lib/modprobe.d/${_pkgname}.conf'"
	install -D -m 644 "${srcdir}/xpad/modprobe.conf" "${pkgdir}/usr/lib/modprobe.d/${_pkgname}.conf"
}
