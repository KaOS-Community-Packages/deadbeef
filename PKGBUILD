pkgname=deadbeef
pkgver=0.7.2
pkgrel=1
pkgdesc="Music player for *nix-like systems and OS X"
url='http://deadbeef.sourceforge.net'
arch=('x86_64')
license=('GPL2')
depends=('gtk2' 'gtk-update-icon-cache' 'alsa-lib' 'hicolor-icon-theme' 'desktop-file-utils' 'curl' 'jansson' 'libvorbis' 'libmad' 'flac' 'imlib2' 'wavpack' 'libsndfile' 'libcdio'
        'libcddb' 'libx11' 'faad2' 'zlib' 'pulseaudio' 'libzip' 'libsamplerate' 'yasm' 'ffmpeg' 'mpg123' 'libcdio-paranoia')
makedepends=('intltool' 'pkg-config')
install='deadbeef.install'
source=("http://downloads.sourceforge.net/project/${pkgname}/${pkgname}-${pkgver}.tar.bz2")
md5sums=('eeeefd13f6220b564582afacf658f463')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr --enable-gtk2 --disable-gtk3
  make
}

package() {
 cd "${srcdir}/${pkgname}-${pkgver}"
 make prefix="${pkgdir}/usr" install
  }
