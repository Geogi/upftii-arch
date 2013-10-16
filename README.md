ULTIMATE PRO FIGHTER TURBO II - Arch Linux PKGBUILD
===================================================

I use it to test UPFTII on my setup.

Dirty one liner to update the game locally (without version bump, including Arch's):

  git clean -fd; git clean -fXd; autoreconf -i && ./configure && make dist && SUM=`sha1sum upftii-0.2.1.tar.gz | cut -d' ' -f1` && (cd ../upftii-arch; sudo pacman -R upftii; rm -r pkg src *.xz; mv ../upftii/*.tar.gz .;  sed -i'~' 's/sha1sums=(.*/sha1sums=('"'"$SUM"'"')/' PKGBUILD; makepkg && sudo pacman -U *.xz && upftii)
