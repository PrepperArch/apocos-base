pkgname=apocos-base
pkgver=0.0.3
pkgrel=1
pkgdesc="Base system configuration for Apocalypse OS"
arch=('any')
url="https://github.com/PrepperArch/apocos-base"
license=('MIT')
install="$pkgname.install"
source=(
    'sudoers.wheel'
)
sha256sums=(
    'baefbd6804946a4e2da608f0ca73ff4936cbf1582cc97d416f75837e68323e26'
)
depends=(
    # System
    'linux' 'linux-firmware' 'mkinitcpio'

    # Services
    'dbus' 'bluez' 'bluez-utils' 'power-profiles-daemon'

    # Audio
    'alsa-utils'
    'pipewire' 'wireplumber' 'pipewire-audio' 'pipewire-alsa'

    # Network
    'dhcpcd' 'networkmanager' 'firewalld' 'curl'

    # Utilities
    'bat' 'brightnessctl' 'less' 'tmux' 'sudo'

    # Editors
    'neovim'
)

package(){
    # setup sudoers
    install -Dm0644 sudoers.wheel $pkgdir/etc/sudoers.d/wheel
}

