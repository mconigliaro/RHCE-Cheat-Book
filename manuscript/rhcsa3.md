# Configure local storage

## List, create, delete partitions on MBR and GPT disks

List partitions:

    parted <device> print

Create partition:

    parted <device> mkpart <type> <start> <end>

Delete partition:

    parted <device> rm <partition number>

## Create and remove physical volumes, assign physical volumes to volume groups, and create and delete logical volumes

Create physical volume:

    pvcreate <device>

Remove physical volume:

    pvremove <device>

Create volume group:

    vgcreate <name> <pv device> [pv device] ...

Extend volume group:

    vgextend <name> <pv device>

Create logical volume:

    lvcreate --size <size>M --name <lv name> <vg name>

Delete logical volume:

    lvremove <lv name>

## Configure systems to mount file systems at boot by Universally Unique ID (UUID) or label

## Add new partitions and logical volumes, and swap to a system non-destructively
