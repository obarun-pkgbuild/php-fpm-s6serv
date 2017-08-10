# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=php-fpm-s6serv
pkgver=0.1
pkgrel=1
pkgdesc="php-fpm service for s6"
arch=(x86_64)
license=('beerware')
depends=('php-fpm' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('php-fpm.daemon.run.s6'
		'LICENSE')
md5sums=('7c18ca8bb20ba030161c191a5cc362ca'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/php-fpm.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/php-fpm/run"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/php-fpm-s6serv/LICENSE"
}
