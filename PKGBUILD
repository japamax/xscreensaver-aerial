# Contributor: Christophe LAVIE <christophe.lavie@laposte.net> 02/11/2017

pkgname='xscreensaver-aerial'
_gitname='xscreensaver-aerial'
pkgver=1.08
pkgrel=1
arch=('any')
url="https://github.com/japamax/xscreensaver-aerial"
license=('MIT')
pkgdesc='xscreensaver hack that randomly selects one of the Apple TV4 HD aerial movies'
depends=('xscreensaver' 'mpv')
optdepends=('xscreensaver-aerial-videos: pre-downloaded videos to save bandwidth')
install=readme.install
source=("git+http://github.com/japamax/xscreensaver-aerial")
sha256sums=('SKIP')

pkgver() {
  cd $_gitname
  git describe --tags --long | sed -r 's/^v//;s/([^-]*-g)/r\1/;s/-/./g'
}


package() {
    cd $_gitname
	install -Dm755 atv4.sh "${pkgdir}/usr/lib/xscreensaver/atv4"
	install -Dm644 MIT "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
	install -Dm644 "${srcdir}/atv4.xml" "${pkgdir}/usr/share/xscreensaver/config/atv4.xml"
}
