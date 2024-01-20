# Maintainer: Dušan Simić <dusan.simic1810@gmail.com>

pkgname=nitch
pkgver=0.1.6
_commit=73819b1
pkgrel=3
pkgdesc="Incredibly fast system fetch written in nim"
arch=(x86_64)
url=https://github.com/hewol/aeros-nitch
license=(MIT)
makedepends=(nim git openssl-1.1)
source=("git+$url#commit=$_commit")
md5sums=(SKIP)

build() {
    mv aeros-nitch nitch
	cd "$pkgname"
	nimble build
}

package() {
	cd "$pkgname"
	install -Dm755 -t "$pkgdir/usr/bin" "$pkgname"
	install -Dm644 -t "$pkgdir/usr/share/licenses/$pkgname" LICENSE
}
