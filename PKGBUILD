pkgname=gh-release-checker
pkgver=1.0
pkgrel=1
pkgdesc="Track GitHub repository releases and get notifications."
arch=('any')
url="https://github.com/chenxing-dev/gh-release-checker"
license=('GPL3')
depends=('curl' 'jq' 'libnotify')
source=("gh-release-checker")
install=gh-release-checker.install

package() {
    install -Dm755 "$srcdir/gh-release-checker" "$pkgdir/usr/bin/gh-release-checker"
    install -Dm644 /dev/null "$pkgdir/etc/skel/.config/gh-release-checker/repos.conf"
}
