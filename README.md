# GlobalProtect Arch Package

My first attempt at building a package for Arch Linux.

## Usage

1. Have `base-devel` package installed.
2. Clone this repository and change directory into the repository.
3. Fetch and place the source package you got from GlobalProtect. It will have the filename like `PanGPLinux-5.1.4-c9.tgz`.
4. Run `makepkg -si`

**Note:** If version changed, you'll need to change the `pkgver` and `sha256sums` fields

```bash
sudo pacman -S base-devel
git clone https://github.com/mbtamuli/GlobalProtect-Arch.git
cd GlobalProtect-Arch
# Download PanGPLinux-5.1.4-c9.tgz - use `wget http://example.com/PanGPLinux-5.1.4-c9.tgz`
makepkg -si
```