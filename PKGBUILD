pkgname=apocos-base
pkgver=0.0.4
pkgrel=4
pkgdesc="Base system configuration for Apocalypse OS"
arch=('any')
url="https://github.com/PrepperArch/apocos-base"
license=('MIT')
install="$pkgname.install"
source=(
    'sudoers.wheel'
    'background.jpg'
)
sha256sums=(
    'baefbd6804946a4e2da608f0ca73ff4936cbf1582cc97d416f75837e68323e26'
    'a7c9a34ad66889cf58c874985ebc348fa2b0c4f2b5248f933510c8fe75a2201b'
)
depends=(
    # System
    'linux' 'linux-firmware' 'mkinitcpio' 'man-db' 'acpi'

    # Services
    'dbus' 'bluez' 'bluez-utils' 'power-profiles-daemon'

    # Audio
    'alsa-utils'
    'pipewire' 'wireplumber' 'pipewire-audio' 'pipewire-pulse' 'pipewire-alsa'

    # Network
    'dhcpcd' 'networkmanager' 'firewalld' 'curl'

    # Utilities
    'bat' 'brightnessctl' 'which' 'less' 'tmux' 'sudo'

    # Editors
    'neovim'
)

package(){
    # setup sudoers
    install -Dm0644 sudoers.wheel $pkgdir/etc/sudoers.d/wheel
    
    install -Dm0644 background.jpg  $pkgdir/usr/share/apocos/background.jpg
}

