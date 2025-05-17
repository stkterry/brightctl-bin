# Maintainer: Steven Terry <https://github.com/stkterry>

_pkgname=brightctl
pkgname=$_pkgname-bin
pkgver=0.9.0
pkgrel=1
pkgdesc="Device brightness control for systemd"
arch=('x86_64')
url=https://github.com/stkterry/$_pkgname
license=('MIT')
depends=('systemd-libs')
makedepends=('git')
source=(
	$_pkgname-$pkgver.tar.gz::$url/archive/v$pkgver.tar.gz
	$url/releases/download/v$pkgver/$_pkgname
)
provides=($_pkgname)
conflicts=($_pkgname)
md5sums=('SKIP' 'SKIP')
options=(!strip)

package() {
	install -Dm755 $_pkgname $pkgdir/usr/bin/$_pkgname
	cd $_pkgname-$pkgver
	install -Dm644 ./LICENSE $pkgdir/usr/share/licenses/$_pkgname/LICENSE
}
