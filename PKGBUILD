# Maintainer: Arne Ko <arneko  at   yahoo  com>
# Contributor: Randy Heydon <randy dot heydon at clockworklab dot net> 
 
pkgname=openmodelica-bin
pkgver=1.9.0beta4
pkgrel=3
pkgdesc="The Open Source Modelica Compiler - precompiled binary"
arch=('i686' 'x86_64')
url="https://www.openmodelica.org"
license=('GPL3' 'custom:OSMC-PL')
depends=('sh' 'omniorb' 'lpsolve' 'sqlite3' 'soqt' 'qwt5' 'f2c')
if [[ $CARCH == 'i686' ]]; then
source=('https://build.openmodelica.org/tar-xz/openmodelica-i386-release.tar.xz' 
'OSMC-License.txt')
md5sums=('SKIP' 
'cf024b4b40f7a2b73beeb8b017c119b6')
else
source=('https://build.openmodelica.org/tar-xz/openmodelica-amd64-release.tar.xz' 
'OSMC-License.txt')
md5sums=('SKIP' 
'cf024b4b40f7a2b73beeb8b017c119b6')
fi
options=(!strip)
 
package() {
cp -r "$srcdir/usr" "$pkgdir"
ln -s /usr/lib/liblapack.so.3 "$pkgdir/usr/lib/liblapack.so.3gf"
ln -s /usr/lib/libblas.so.3 "$pkgdir/usr/lib/libblas.so.3gf"
ln -s /usr/lib/libqwt5.so "$pkgdir/usr/lib/libqwt-qt4.so.5"
install -Dm 644 "./OSMC-License.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
