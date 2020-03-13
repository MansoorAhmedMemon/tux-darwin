# Tux Darwin
An OS X flavored plymouth for Linux Ubuntu [with Tux logo].

## Installation

Add `tux-darwin` to your `plymouth` themes directory.

    sudo cp -R tux-darwin /usr/share/plymouth/themes/tux-darwin
    
Add `tux-darwin` to `default.plymouth`'s alternatives

    sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/tux-darwin/tux-darwin.plymouth 10

To use the newly installed alternative, run

    sudo update-alternatives --config default.plymouth
    
and select `tux-darwin`.

Finally update your `initramfs` to see changes on reboot

    sudo update-initramfs -u
    
### Uninstalling

    sudo update-alternatives --remove default.plymouth /usr/share/plymouth/themes/tux-darwin/tux-darwin.plymouth
    sudo rm -R /usr/share/plymouth/themes/tux-darwin
    sudo update-initramfs -u
    
    
## Credits
Copied from the copy darwin plymouth [with Ubuntu Logo]: https://github.com/ashutoshgngwr/ubuntu-darwin.git which is derived from the original darwin plymouth [with Apple Logo]: https://www.gnome-look.org/content/show.php/Darwin+Plymouth?content=170649