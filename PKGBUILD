#aintainer: djawna@gmail.com
_pkgname=xpad-dja
pkgname=xpad-dja-dkms
pkgver=0.4
pkgrel=3
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
	'fakeroot'
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
source=(
	'git+https://github.com/DJawna/xpad.git#commit=e83036d'
	'modprobe.conf'
)
noextract=()
sha256sums=(
	'SKIP'
	'SKIP'
)
validpgpkeys=()

prepare() {
	echo "patching in the modprobe file"
	cp ./modprobe.conf "${srcdir}/xpad/modprobe.conf"
}

package() {
	echo "* installing /usr/src"
	install -dm644 "${pkgdir}/usr/src/${_pkgname}-${pkgver}"

	echo "* copying module into /usr/src..."
	cp -r "${srcdir}/xpad/"* "${pkgdir}/usr/src/${_pkgname}-${pkgver}/"
	chmod 755 "${pkgdir}/usr/src/${_pkgname}-${pkgver}/"
	
	echo "install blacklist '${srcdir}/xpad/modprobe.conf' -> '${pkgdir}/usr/src/lib/modprobe.d/${_pkgname}.conf'"
	install -D -m 644 "${srcdir}/xpad/modprobe.conf" "${pkgdir}/usr/lib/modprobe.d/${_pkgname}.conf"

}
