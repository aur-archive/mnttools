# Maintainer: trile7 at gmail dot com

pkgname=mnttools
pkgver=0.4.5
pkgrel=2
pkgdesc="Mount tools for usb drive, sd card, optical disc, image file, SSH, FTP, or Samba.  Automatically mount usb drive and sd card on insert via udev rules."
url="http://bashscripts.googlecode.com"
arch=('any')
license=('GPL3')
depends=(coreutils procps-ng grep sudo util-linux bash)
optdepends=("yad: display trayicon" "lsof: list open files" "smbclient: browse and mount Samba/Windows network" "sshfs: mount SSH" "curlftpfs: mount FTP")
source=($url/files/$pkgname-$pkgver.tar.gz)

package() {
  cd "$srcdir/$pkgname-$pkgver"
  mkdir -p "$pkgdir/usr/share/$pkgname" "$pkgdir/usr/bin"
  mkdir -p "$pkgdir/etc/udev/rules.d"
  cp * "$pkgdir/usr/share/$pkgname"
  ln -s /usr/share/$pkgname/$pkgname "$pkgdir/usr/bin/$pkgname"
  install -Dm 644 $pkgname.rules "$pkgdir/etc/udev/rules.d/80-$pkgname.rules"
}

md5sums=('09ef01c14760cfd7e5c53f80f2f87454')
