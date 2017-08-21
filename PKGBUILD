# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=php-fpm-s6serv
pkgver=0.2
pkgrel=2
pkgdesc="php-fpm service for s6"
arch=(x86_64)
license=('beerware')
depends=('php-fpm' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('php-fpm.daemon.run.s6'
		'php-fpm.log.run.s6'
		'php-fpm.logd'
		'LICENSE')
md5sums=('0dc428502021661da5636272293e36b0'
         '9f89c1b468e593961fc86a94b7bfb25a'
         '065977df1c71010171bc36e895c510ce'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/php-fpm.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/php-fpm/run"
	
	#log
	install -Dm 0755 "$srcdir/php-fpm.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/php-fpm/log/run"
	install -Dm 0644 "$srcdir/php-fpm.logd" "$pkgdir/etc/s6-serv/log.d/serv/php-fpm"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/php-fpm-s6serv/LICENSE"
}
