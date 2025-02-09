# Maintainer: Breno Ramalho Lemes <breno@br-lemes.net>
pkgname=kanata-bin
pkgver=1.8.0
pkgrel=1
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
	'd3644a07164be46c3d507cffed5e3b2838dc08dcdd9b2e62f5906ce8b5ea0578'
	'1466e42d1c6e3e164e6bb6899167c03e424a2d5aea8ff136e114591d0569129c'
	'a5681bf9b05db14d86776930017c647ad9e6e56ff6bbcfdf21e5848288dfaf1b'
)

package() {
	install -Dm755 "kanata-${pkgver}" "${pkgdir}/usr/bin/kanata"
	install -Dm755 "kanata_cmd_allowed-${pkgver}" "${pkgdir}/usr/bin/kanata_cmd_allowed"
	install -Dm644 LICENSE -t "${pkgdir}/usr/share/licenses/${pkgname}"
}
