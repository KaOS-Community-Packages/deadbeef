
pkgname=deadbeef
pkgver=6.2.1
_commit=593c1c1e5fb2aab32028e1fed3fe51481270f651
pkgrel=1
pkgdesc="Music player for *nix-like systems and OS X"
url="https://github.com/Alexey-Yakovenko/deadbeef"
arch=('x86_64')
license=('GPL2')
depends=('alsa-lib' 'desktop-file-utils' 'gtk2' 'hicolor-icon-theme' 'jansson' 'curl' 'faad2' 'flac'
         'imlib2' 'libcddb' 'libcdio' 'libmad' 'pulseaudio' 'libsamplerate' 'libvorbis' 'libx11' 'libzip'
         'wavpack' 'yasm')
makedepends=('git' 'intltool')
install='deadbeef.install'
options=('!libtool')
source=("https://github.com/Alexey-Yakovenko/deadbeef/archive/${_commit}.zip")
md5sums=('bab70aac2b0bf3428f1031fc413388bb')

build() {
  cd ${srcdir}/${pkgname}-${_commit}

  ./autogen.sh
  ./configure --prefix=/usr --enable-ffmpeg --enable-gtk2 --disable-gtk3
  
  make
}

package() {
  cd ${srcdir}/${pkgname}-${_commit}

  make DESTDIR=${pkgdir} install
}
