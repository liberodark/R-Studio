# Maintainer: liberodark

pkgname=r-studio
pkgver=4.2.2901
pkgrel=1
pkgdesc="Undelete and data recovery software"
arch=('i686' 'x86_64')
url="http://www.r-tt.com/data_recovery_linux/"
license=('custom')
depends=('xdg-utils')
source_i686=("http://www.r-studio.com/downloads/RStudio4_i386.deb")
source_x86_64=("http://www.r-studio.com/downloads/RStudio4_x64.deb")
source=($pkgname.desktop
        $pkgname.png)
        
package() {
  cd $srcdir
  tar xvf data.tar.gz
  cp -r usr $pkgdir
  rm $pkgdir/usr/local/R-Studio/share/{logo*,*.desktop}	
  rm $pkgdir/usr/bin/rstudio
  ln -sr /usr/local/R-Studio/bin/R-Studio $pkgdir/usr/bin/R-Studio
  install -vDm644 $srcdir/$pkgname.desktop $pkgdir/usr/share/applications/$pkgname.desktop
  install -vDm644 $srcdir/$pkgname.png $pkgdir/usr/share/pixmaps/$pkgname.png
}

md5sums=('023626f715a2581768dac0c6de07ebae'
         '21f1baf671cd9c49c740d92b506203f9')
md5sums_i686=('9b2d7fba8fd201a7f3236706b5e7843f')
md5sums_x86_64=('6bbb7c66414e0593bae528d4985a03c0')