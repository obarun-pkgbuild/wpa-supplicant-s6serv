# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=wpa-supplicant-s6serv
pkgver=0.1
pkgrel=4
pkgdesc="wpa-supplicant service for s6"
arch=(x86_64)
license=('beerware')
depends=('wpa_supplicant' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('wpa-supplicant.daemon.run.s6'
		'wpa-supplicant.log.run.s6'
		'wpa-supplicant.logd'
		'LICENSE')
md5sums=('488689115508887d2fd495e15839c8c6'
         '9e69b5a779089438332f23813f614b67'
         'b8015e29aca7c3ebd920be1dcfaa7253'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/wpa-supplicant.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/wpa-supplicant/run"
	
	# log
	install -Dm 0755 "$srcdir/wpa-supplicant.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/wpa-supplicant/log/run"
	install -Dm 0644 "$srcdir/wpa-supplicant.logd" "$pkgdir/etc/s6-serv/log.d/wpa-supplicant"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/wpa-supplicant-s6serv/LICENSE"
}
