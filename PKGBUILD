# Maintainer: Justin Willmert <justin@jdjlab.com>
pkgname=weekly-clamscan
pkgver=0.9
pkgrel=1
pkgdesc="Runs a weekly system-wide scan for viruses using clamscan"
arch=(any)
url=""
install=${pkgname}.install
license=('MIT')
depends=(systemd clamav)
source=(
    "50-clamscan.rules"
    "clamscan.service"
    "clamscan.timer"
    )
md5sums=(
    e7f8a4b6564b5dc8d1365b67ddb10593
    1e77a74584539ca23399848b597bab9d
    9eb0b70a30e47f8379665d6fcbe2753c
    )


package() {
    install -D -m 644 50-clamscan.rules "${pkgdir}"/etc/udev/rules.d/50-${pkgname}.rules
    install -D -m 644 clamscan.service "${pkgdir}"/etc/systemd/system/${pkgname}.service
    install -D -m 644 clamscan.timer "${pkgdir}"/etc/systemd/system/${pkgname}.timer
}

