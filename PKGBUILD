
pkgname=deadbeef
pkgver=6.2.2
_commit=d83311c4e82b6fdd6afe6da2cc9bcd8b195042be
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
md5sums=('c3fccf362d5c0e83c59dac260ac96bd5')

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
