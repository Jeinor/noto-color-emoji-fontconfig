# Maintainer: Kevin Del Castillo R. <quebin31@gmail.com>

pkgname=noto-color-emoji-fontconfig
pkgver=1.0.0
pkgrel=2
pkgdesc='Fontconfig to enable Noto Color Emoji fonts where emojis can be displayed'
arch=('any')
license=('GPL')
depends=('noto-fonts-emoji')
optdepends=()
provides=('noto-color-emoji-fontconfig')
conflicts=('noto-color-emoji-fontconfig-no-binding')
options=()
source=('75-noto-color-emoji.conf')
sha256sums=('9b7d8e078e0f88582afc8f19cd7d928a6bd2b2f418321d1011d4d6f903056942')

package() {
    local conf_avail='usr/share/fontconfig/conf.avail/'
    local conf_d='usr/share/fontconfig/conf.default/'

    install -Dm655 '75-noto-color-emoji.conf' -t "${pkgdir}/${conf_avail}"
    mkdir -p "${pkgdir}/${conf_d}"
    ln -s "/${conf_avail}/75-noto-color-emoji.conf" "${pkgdir}/${conf_d}"
}
