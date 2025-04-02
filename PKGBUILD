# Maintainer: Breno Ramalho Lemes <breno@br-lemes.net>
pkgname=kanata-bin
pkgver=1.8.1
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
	'7c123b3897af15e8520e439acde4c9be0c50ccd810a60273d84295750eec4921'
	'6a4f05fa050a23ff2e1b35be56ad26fc62ca5bc7f5a8c20d7395569fa8e88d2d'
	'a5681bf9b05db14d86776930017c647ad9e6e56ff6bbcfdf21e5848288dfaf1b'
)

package() {
	install -Dm755 "kanata-${pkgver}" "${pkgdir}/usr/bin/kanata"
	install -Dm755 "kanata_cmd_allowed-${pkgver}" "${pkgdir}/usr/bin/kanata_cmd_allowed"
	install -Dm644 LICENSE -t "${pkgdir}/usr/share/licenses/${pkgname}"
}
