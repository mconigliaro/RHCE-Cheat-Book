# Operate running systems

## Boot, reboot, and shut down a system normally

Pressing the power button is "normally" enough to boot a system.

To reboot:

    systemctl reboot

To shut down:

    systemctl poweroff

## Boot systems into different targets manually

First, get a list of available target units:

    systemctl list-units --type target --all

To boot into a new target:

    systemctl isolate <name>.target

## Interrupt the boot process in order to gain access to a system

1. At the GRUB2 boot loader menu, highlight an entry and type `e` to edit it
2. On the line beginning with `linux`, replace `rhgb` with `init=/bin/sh`
3. Type `Ctrl`+`x` to continue booting the system
4. Load the SELinux policy: `/usr/sbin/load_policy -i`
5. Remount the root partition as read-write: `mount -o remount,rw /`
6. Reset the root password: `passwd root`
7. Remount the root partition as read-only: `mount -o remount,ro /`
8. Reboot the system: `systemctl reboot`

## Identify CPU/memory intensive processes, adjust process priority with renice, and kill processes

Identify CPU/memory intensive processes:

    top

Adjust process priority:

    renice <priority> <pid>

Kill processes:

    kill [-9] <pid>

## Locate and interpret system log files and journals

System logs are written under `/var/log`. Systemd journals can be inspected using the `journalctl` command.

## Access a virtual machine's console

    virsh console <domain>

## Start and stop virtual machines

    virsh start <domain>
    virsh stop <domain>

## Start, stop, and check the status of network services

    systemctl start <service>
    systemctl stop <service>
    systemctl status <service>

## Securely transfer files between systems

    scp [options] <src> <dst>
