# Maintainer: jsteel <mail at jsteel dot org>
# Contributor: pumbur <pumbur@ya.ru>

pkgname=gtk-theme-shiki-colors-flat
pkgver=1
pkgrel=3
pkgdesc="Shiki-Colors GTK+ theme (flat version)"
arch=('any')
url="http://spktkpkt.deviantart.com/art/Shiki-Colors-Flat-130378438"
license=('GPL')
depends=('gtk-engine-murrine')
optdepends=('openbox-shikidark-colors-themes: For Openbox users')
source=(http://pkgbuild.com/~jsteel/aur/gtk-theme-shiki-colors-flat/Shiki_Colors_Flat_by_spktkpkt.zip)
md5sums=('af9dfc95b0cc56d316b2d8e3a867b20d')

package() {
  install -dm755 "$pkgdir"/usr/share/themes

  cd "$pkgdir"/usr/share/themes

  for i in Brave-Flat Dust-Flat Human-Flat Illustrious-Flat Noble-Flat Tribute-Flat Wine-Flat Wise-Flat; do
    tar -zxvf "$srcdir"/Shiki-$i.tar.gz
    # remove the gradients option which is no longer supported
    sed -i '/gradients/d' Shiki-$i/gtk-2.0/gtkrc
  done

  tar -zxvf  "$srcdir"/Shiki-Colors-Flat-Metacity.tar.gz

  chown -R root:root "$pkgdir"/usr/share/themes/*
}
