# $Id: PKGBUILD 356 2008-04-18 22:56:27Z aaron $
# Maintainer: Lou Greenwood <lou@archlinux.org>

pkgname=trm
pkgver=0.2.1
pkgrel=2
pkgdesc="Allows multimedia apps to lookup ID3 tags from the Internet."
arch=('i686' 'x86_64')
url="http://www.musicbrainz.org/products/trmgen/download.html"
license=()
depends=('musicbrainz')
md5sums=('3f7e6c30cb91429313ca1a27df47e8bc')

source=(ftp://ftp.musicbrainz.org/pub/musicbrainz/$pkgname-$pkgver.tar.gz)


build() {
        cd $startdir/src/$pkgname-$pkgver
        ./configure --prefix=/usr
        make || return 1
	mkdir $startdir/pkg/usr
	mkdir $startdir/pkg/usr/bin
        make prefix=$startdir/pkg/usr install || return 1
}
