# Installing Vundle

1. Git clone VundleVim/Vundle.vim
2. Ln -s into ~/.vim/bundle
3. From VI do Vundle install

# Burning media

1. Mount point
  - Fedora automount
    - /run/media/<user>/CDROM/
  - Manual mounting
    - # mount /dev/dvd /media
2. Create iso
  - $ mkisofs -JR -V -o <isoname> <head_of_foler_becomes_root>
3. Burn
  - Linux
    - cdrecord <isoname>
  - Windows
    - Copy to Windows
    - Right click, burn image to disk
4. Eject media
  - Should be automatic
  - # eject


