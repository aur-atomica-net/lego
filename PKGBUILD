# Maintainer: Jason R. McNeil <jason@jasonrm.net>

pkgname=lego
pkgver=0.3.0
pkgrel=1
pkgdesc="Let's Encrypt client and ACME library written in Go"
arch=('i686' 'x86_64' 'armv6h')
url="https://github.com/xenolf/lego"
license=('MIT')

source=('lego.service' 'lego.timer' 'lego.env')
sha256sums=('edfdb149499f75213dcac99cd19d821e49fd2595a566ff861f6ead18003f1c99'
            '3b2b42db3665795186301b9c979a74a32bf14a6025629fcca388581450f5a598'
            '499a12400e02c379f755689439390aa903ce3f67716a1079ad388cb8cbfe6d68')
sha256sums_i686=('a4e674df3873e556356abeba1d0bc60b4667dafd37529020710abd8e03ed661b')
sha256sums_x86_64=('796ce5cb3553f301fcf95f60217f24549077629dfd2c07428171508eb8574350')
sha256sums_armv6h=('51262840324d31eb0bf4c2a38cc5955130a6d073ce9658bd4c8113f935628833')

source_i686=("https://github.com/xenolf/lego/releases/download/v$pkgver/lego_linux_386.tar.xz")

source_x86_64=("https://github.com/xenolf/lego/releases/download/v$pkgver/lego_linux_amd64.tar.xz")

source_armv6h=("https://github.com/xenolf/lego/releases/download/v$pkgver/lego_linux_arm.tar.xz")

package() {
    install -Dm755 ${srcdir}/lego/lego ${pkgdir}/usr/bin/lego
    install -Dm644 ${srcdir}/lego.service ${pkgdir}/usr/lib/systemd/system/lego.service
    install -Dm644 ${srcdir}/lego.timer ${pkgdir}/usr/lib/systemd/system/lego.timer

    install -Dm644 ${srcdir}/lego.env ${pkgdir}/etc/conf.d/lego
}
