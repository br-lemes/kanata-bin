# Maintainer: Breno Ramalho Lemes <breno@br-lemes.net>
pkgname=kanata-bin
pkgver=1.7.0
pkgrel=2
pkgdesc='Improve keyboard comfort and usability with advanced customization'
arch=('x86_64')
url='https://github.com/jtroo/kanata/'
license=('LGPL-3.0-only')
provides=('kanata')
depends=('gcc-libs' 'glibc')
source=(
	"kanata-${pkgver}::https://github.com/jtroo/kanata/releases/download/v${pkgver//_/-}/kanata"
	"kanata_cmd_allowed-${pkgver}::https://github.com/jtroo/kanata/releases/download/v${pkgver//_/-}/kanata_cmd_allowed"
	'https://github.com/jtroo/kanata/raw/main/LICENSE'
)
sha256sums=(
	'03f2dc888fc7831d50f55fc1ff5dcb1fc1015616a85529cbb936c3bbc4af1326'
	'1c2bdfcb2a40a0228ca5d9cfcf0cfab84b17cf1aa8b39dcd22bdebdfc72a6660'
	'a5681bf9b05db14d86776930017c647ad9e6e56ff6bbcfdf21e5848288dfaf1b'
)

package() {
	install -Dm755 "kanata-${pkgver}" "${pkgdir}/usr/bin/kanata"
	install -Dm755 "kanata_cmd_allowed-${pkgver}" "${pkgdir}/usr/bin/kanata_cmd_allowed"
	install -Dm644 LICENSE -t "${pkgdir}/usr/share/licenses/${pkgname}"
}
