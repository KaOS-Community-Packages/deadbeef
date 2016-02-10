
pkgname=deadbeef
pkgver=0.7.0
pkgrel=1
pkgdesc="Music player for *nix-like systems and OS X"
url='http://deadbeef.sourceforge.net'
arch=('x86_64')
license=('GPL2')
depends=('gtk3' 'alsa-lib' 'hicolor-icon-theme' 'desktop-file-utils' 'jansson')
makedepends=('libvorbis' 'libmad' 'flac' 'curl' 'imlib2' 'wavpack' 'libsndfile' 'libcdio' 'libcddb'
             'libx11' 'faad2' 'zlib' 'intltool' 'pkg-config' 'pulseaudio' 'libzip' 'libsamplerate'
             'yasm' 'ffmpeg' 'gtk-update-icon-cache' 'mpg123' 'libcdio-paranoia')
install='deadbeef.install'
source=("http://downloads.sourceforge.net/project/${pkgname}/${pkgname}-${pkgver}.tar.bz2")
md5sums=('d5450785139757a016dcd4dfc66479c7')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr  
  make
}

package() {
 cd "${srcdir}/${pkgname}-${pkgver}"
 make prefix="${pkgdir}/usr" install
  }
