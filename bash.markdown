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
  - $ mkisofs -JR -V -o <isoname_eg_CDROM> <head_of_foler_becomes_root>
3. Burn
  - Linux
    - cdrecord <isoname>
  - Windows
    - Copy to Windows
    - Right click, burn image to disk
4. Eject media
  - Should be automatic
  - # eject

# Debugging core files, object/archive files, binaries

- $ file <..>
- $ ldd -v <..>  # on dynamic executables
- $ nm -a <..>
- $ readelf -a <..>
- $ strings <..> | less
- $ stat <..>
- $ gdb <progname> <corefile>
- $ objdump -fx <..> | less  # -d, can get assembler instrucitons etc
- $ xxd <..> | head

# Bash builtins

## Testing existance of command

- command -v <command> >/dev/null 2>&1 || { echo >&2 "Blah..."; exit 1; }

# Memory/CPU info

- $ procinfo -a
- $ htop
- $ cat /proc/cpuinfo
- $ cat /proc/meminfo
- $ cat /proc/loadavg

# Examining storage, devices, media

- $ lsblk  # aliased
- # fdisk -l
- $ cat /proc/devices
- $ mount
  - or $ cat /proc/mounts
- $ cat /proc/partitions; # file -s /dev/<partition> (or # parted <..> print)
- $ cat /proc/interrupts
- General info also in /proc/sys such as /fs/
  - E.g. $ cat /proc/sys/dev/cdrom/info

# Unmounting USB

1. # umount /media/<device>

# Shared memory/semaphores

- $ ipcs -ma # List SHM/SEM
  - or  $ cat /proc/sysvipc/shm
  - and $ cat /proc/sysvipc/sem
- $ ipcs -pa # PID of creator/last
- # lsof|egrep "^COMMAND|<key>"
- $ grep <pid> /proc/*/maps # Find owners

# Who has a file/desciptor/etc open

- # lsof </path/to/filename>
  - or fuser <..>
- # dgrep <filename> # alias, bash completion not regex

# Running process tasks

## Info about process

### General

- $ psi <pid> # alias
- # lsof <pid> # or lsof|egrep "^COMMAND|<name>"
- From /proc/<pid>/ as root
  - ll exe       # Executable link
  - ll cwd       # CWD
  - ll fd        # Open file descriptors
  - ll map_files # Lib maps
  - cat status   # Misc process info (see $ psi)
  - cat cmdline  # Call that was made
  - cat environ  # Current environment
  - cat maps     # Memory maps
  - cat smaps    # Breakdown of maps

### Memory

#### Actual

- # pmap -x <pid>
  - or # cat /proc/<pid>/smaps

#### Allocated

- $ psi <pid>

## Find process

- $ htop (or top)
- $ ps auxf | egrep <name>
- $ pgrep -u <user> <name>
- $ pts # get your tty no

## Killing a process

- With PID
  - $ kill <pid> # SIGTERM
  - $ kill -1 <pid> # SIGHUP
  - $ kill -9 <pid> # SIGKILL, last resort
  - $ pkill <pid> # SIGTERM default
- With name
  - $ killall <name> # Regex OK
  - $ pkill -f <name> # SIGTERM default

## Debugging a running process

- $ valgrind --tool=massif # TODO

# Change resolution of monitor over ssh

1. $ ssh <login> # Without X forwarding
2. $ export DISPLAY=:0
3. $ xrandr --verbose
  - Note the Identifier (e.g. 0xf0)
5. $ xrandr --output <identifier> --mode <mode_from_verbose_list>
  - E.g. $ xrandr --output 0xf0 --mode 800x600

# Shutting down, rebooting

1. # shutdown -h now # shutting down immediately and halting now
2. # reboot

