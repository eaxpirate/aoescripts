aoescripts
==========

Random scritps for ATA-Over-Ethernet target/initaitor operations

create vblades
==============

This script will spit out some commands you can use to create 
vblade shelves based on a given number of logical volumes in a
given volume group;

This is necessary because a shelf can only have 16 slots

For example:

    :::console
    # vgcreate myvg /dev/md0
    # for i in {00..50}; do
      lvcreate -n vm${i} -L 8g myvg
    done
    # VOLUME_GROUP="myvg" ./create_vblades

