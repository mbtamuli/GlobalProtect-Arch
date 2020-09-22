# Maintainer: Mriyam Tamuli <mbtamuli@gmail.com>

pkgname=GlobalProtect
pkgver=5.1.4
pkgrel=1
pkgdesc="A GlobalProtect VPN client"
arch=(x86_64)
license=("GPL")
install=${pkgname}.install
source=("PanGPLinux-${pkgver}-c9.tgz")
sha256sums=("1f939ca2f6ff9ae603bec5c4e952c618499764d97db0bd8b9c49e5dca54e06d4")

package() {
	tar xf GlobalProtect_tar-${pkgver}.0-9.tgz

	install -dm755 "${pkgdir}/opt/paloaltonetworks/globalprotect"

	install -Dm755 "${srcdir}/globalprotect" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/PanGPA" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/PanGpHip" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/PanGpHipMp" "${pkgdir}/opt/paloaltonetworks/globalprotect/"

	install -Dm755 "${srcdir}/libwaapi.so.4.3.1055.0" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/libwaheap.so.4" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/libwalocal.so.4.3.1055.0" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/libwaresource.so" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/libwautils.so.4.3.1055.0" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/libwaapi.so" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/libwaapi.so.4" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/libwaheap.so" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/libwalocal.so" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/libwalocal.so.4" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/libwautils.so" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/libwautils.so.4" "${pkgdir}/opt/paloaltonetworks/globalprotect/"

	install -Dm644 "${srcdir}/license.cfg" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/pre_exec_gps.sh" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm755 "${srcdir}/uninstall.sh" "${pkgdir}/opt/paloaltonetworks/globalprotect/"
	install -Dm644 "${srcdir}/pangps.xml" "${pkgdir}/opt/paloaltonetworks/globalprotect/"

	install -dm755 "${pkgdir}/usr/lib/systemd/system/"
	install -Dm644 "${srcdir}/gpd.service" "${pkgdir}/usr/lib/systemd/system/"

	install -dm755 "${pkgdir}/usr/share/man/man1/"
	install -Dm644 "${srcdir}/globalprotect.1.gz" "${pkgdir}/usr/share/man/man1/"

	install -dm755 "${pkgdir}/usr/local/bin/"
	ln -s "${srcdir}/globalprotect" "${pkgdir}/usr/local/bin/globalprotect"
}