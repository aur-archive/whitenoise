# Maintainer:  TDY <tdy@archlinux.info>
# Contributor: Hannes Rist <cowider@gmail.com>

pkgname=whitenoise
pkgver=1.0.2
pkgrel=1
pkgdesc="An ambient random noise generator"
arch=('i686' 'x86_64')
url="http://pessimization.com/software/whitenoise/"
license=('GPL')
optdepends=('fftw: generate filter frequency plots (rebuild required)'
            'gnuplot: also needed for plots (no rebuild required)')
source=(http://pessimization.com/software/$pkgname/$pkgname-$pkgver.tar.gz
        $pkgname.1)
md5sums=('1066f99e2af2d36a86ae48be8eb1ab1d'
         '55bbda3a2a130126fc77e0227352abe6')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr --disable-arts --disable-fftw
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  install -Dm755 $pkgname "$pkgdir/usr/bin/$pkgname"
  install -Dm644 ../$pkgname.1 "$pkgdir/usr/share/man/man1/$pkgname.1"
}

# vim:set ts=2 sw=2 et:
