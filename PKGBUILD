pkgname=multilogin
provides=(${pkgname})
conflicts=(${pkgname})
pkgver=6.2.0
pkgrel=7
pkgdesc="Replace multiple computers with virtual browser profiles"
arch=('x86_64')
license=("custom")
url="https://multilogin.com/"
depends=(unzip gtk3 libnotify nss openssl xdg-utils python-atspi libcrossguid libsecret)
source=("multilogin.zip::https://cdn-download.multiloginapp.com/multilogin/6.2.0/multilogin-${pkgver}-${pkgrel}-linux_x86_64.zip")
noextract=("multilogin.zip")
sha256sums=("da270f71f62185d001bc83491bc462b596bb03352e092d11d04191f6037d0a4d")
package() {
    cd "${srcdir}"
    unzip "../multilogin.zip" -d "${srcdir}"
    ar x "${srcdir}/multilogin.deb"
    tar -xf "${srcdir}/control.tar.gz"
    tar -xf "${srcdir}/data.tar.xz"
    mkdir -p "${pkgdir}/usr"
    mkdir -p "${pkgdir}/usr/share"
    mkdir -p "${pkgdir}/opt"
    mv "${srcdir}/opt/Multilogin" "${pkgdir}/opt/Multilogin"
    mv "${srcdir}/usr/share/applications" "${pkgdir}/usr/share/applications"
    mv "${srcdir}/usr/share/doc" "${pkgdir}/usr/share/doc"
    mv "${srcdir}/usr/share/icons" "${pkgdir}/usr/share/icons"
}
   
