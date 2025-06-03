# Maintainer: txtdv <mveremeev25@gmail.com>
pkgname=cwatch
pkgver=0.7.0
pkgrel=1
pkgdesc="Continuously watch and display the output of a command, similar to watch or hwatch, but supporting terminal formatting, making commands such as fastfetch properly work, along with colours."
arch=('any')
url="https://www.github.com/textdev-0/cwatch"
license=('MIT')

# Dependencies: python for the interpreter, util-linux for the 'script' command
depends=('python' 'util-linux')

source=("${pkgname}.py")
sha256sums=('5e01f3aa7d0ef5f3b11ae533f336e8b4e82b57377bbb690bbb6af890890f507e') 

source+=("LICENSE")
sha256sums+=('d727d1ca3421c68d924a4c5729913cb8bf0361b7a8cf48fa6fa83053f11a6a5b')


package() {
    # Install the script to /usr/bin/
    # -D creates parent directories if they don't exist
    # -m755 sets permissions to rwxr-xr-x (executable)
    install -Dm755 "${srcdir}/${pkgname}.py" "${pkgdir}/usr/bin/${pkgname}"
    install -Dm644 "${srcdir}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

