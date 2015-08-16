# Maintainer: Christian Babeux <christian.babeux@0x80.ca>
# Contributor: Yggdrasil <tetzank at web dot de>

pkgname=liburcu
pkgver=0.8.6
pkgrel=1
pkgdesc="LGPLv2.1 userspace RCU (read-copy-update) library"
arch=('i686' 'x86_64')
url="http://lttng.org/urcu"
license=('LGPL2.1')
source=(http://lttng.org/files/urcu/userspace-rcu-${pkgver}.tar.bz2)
depends=('glibc')
options=('!libtool')
sha1sums=('f10e9bf812557cd0c2a35a277e04010ec278d25d')

build()
{
    cd ${srcdir}/userspace-rcu-${pkgver}
    ./configure --prefix=/usr
    make
}

package()
{
    cd ${srcdir}/userspace-rcu-${pkgver}
    make install DESTDIR=${pkgdir}
}
