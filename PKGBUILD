# Maintainer: Jason R. McNeil <jason@jasonrm.net>

pkgname=lego
pkgver=0.3.1
pkgrel=1
pkgdesc="Let's Encrypt client and ACME library written in Go"
arch=('i686' 'x86_64' 'armv6h')
url="https://github.com/xenolf/lego"
license=('MIT')
backup=('etc/conf.d/lego')

source=('lego.service' 'lego.timer' 'lego.env')
sha256sums=('2d7aed161e2dc96a5e52236037339e76e7571a9611408996e86987dc9dce180d'
            '3b2b42db3665795186301b9c979a74a32bf14a6025629fcca388581450f5a598'
            '499a12400e02c379f755689439390aa903ce3f67716a1079ad388cb8cbfe6d68')
sha256sums_i686=('c540641ada9e0c55ce2d4c4b51f95ce9d437898f5f3d9a1d105f4c728e4f50fa')
sha256sums_x86_64=('cee9511099e9864968ac9c68f2f8d77fd927cda17957546d99faaf93f310538a')
sha256sums_armv6h=('7c264b2280b11c04e75b71f8d798e8531bc4dfb16ed5ed1e9bbb936bc6a0b941')

source_i686=("https://github.com/xenolf/lego/releases/download/v$pkgver/lego_linux_386.tar.xz")

source_x86_64=("https://github.com/xenolf/lego/releases/download/v$pkgver/lego_linux_amd64.tar.xz")

source_armv6h=("https://github.com/xenolf/lego/releases/download/v$pkgver/lego_linux_arm.tar.xz")

package() {
    install -Dm755 ${srcdir}/lego/lego ${pkgdir}/usr/bin/lego
    install -Dm644 ${srcdir}/lego.service ${pkgdir}/usr/lib/systemd/system/lego.service
    install -Dm644 ${srcdir}/lego.timer ${pkgdir}/usr/lib/systemd/system/lego.timer

    install -Dm644 ${srcdir}/lego.env ${pkgdir}/etc/conf.d/lego
}
