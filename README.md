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

    [root@storage_target vblade-21]# vgcreate myvg /dev/md0
    [root@storage_target vblade-21]# for i in {00..50}; do
      lvcreate -n vm${i} -L 8g myvg
    done
    [root@storage_target vblade-21]# VOLUME_GROUP="myvg" ./create_vblades

    [root@storage_target vblade-21]# ./create_vblades 
    vbladed 0 0 bond0 /dev/mapper/vmstore-vm00
    vbladed 0 2 bond0 /dev/mapper/vmstore-vm02
    vbladed 0 3 bond0 /dev/mapper/vmstore-vm03
    vbladed 0 4 bond0 /dev/mapper/vmstore-vm04
    vbladed 0 5 bond0 /dev/mapper/vmstore-vm05
    vbladed 0 6 bond0 /dev/mapper/vmstore-vm06
    vbladed 0 7 bond0 /dev/mapper/vmstore-vm07
    vbladed 0 8 bond0 /dev/mapper/vmstore-vm08
    vbladed 0 9 bond0 /dev/mapper/vmstore-vm09
    vbladed 0 10 bond0 /dev/mapper/vmstore-vm10
    vbladed 0 11 bond0 /dev/mapper/vmstore-vm11
    vbladed 0 12 bond0 /dev/mapper/vmstore-vm12
    vbladed 0 13 bond0 /dev/mapper/vmstore-vm13
    vbladed 0 14 bond0 /dev/mapper/vmstore-vm14
    vbladed 0 15 bond0 /dev/mapper/vmstore-vm15
    vbladed 0 16 bond0 /dev/mapper/vmstore-vm16
    vbladed 1 17 bond0 /dev/mapper/vmstore-vm17
    vbladed 1 18 bond0 /dev/mapper/vmstore-vm18
    vbladed 1 19 bond0 /dev/mapper/vmstore-vm19
    vbladed 1 20 bond0 /dev/mapper/vmstore-vm20
    vbladed 1 21 bond0 /dev/mapper/vmstore-vm21
    vbladed 1 22 bond0 /dev/mapper/vmstore-vm22
    vbladed 1 23 bond0 /dev/mapper/vmstore-vm23
    vbladed 1 24 bond0 /dev/mapper/vmstore-vm24
    vbladed 1 25 bond0 /dev/mapper/vmstore-vm25
    vbladed 1 26 bond0 /dev/mapper/vmstore-vm26
    vbladed 1 27 bond0 /dev/mapper/vmstore-vm27
    vbladed 1 28 bond0 /dev/mapper/vmstore-vm28
    vbladed 1 29 bond0 /dev/mapper/vmstore-vm29
    vbladed 1 30 bond0 /dev/mapper/vmstore-vm30
    vbladed 1 31 bond0 /dev/mapper/vmstore-vm31
    vbladed 1 32 bond0 /dev/mapper/vmstore-vm32
    vbladed 2 33 bond0 /dev/mapper/vmstore-vm33
    vbladed 2 34 bond0 /dev/mapper/vmstore-vm34
    vbladed 2 35 bond0 /dev/mapper/vmstore-vm35
    vbladed 2 36 bond0 /dev/mapper/vmstore-vm36
    vbladed 2 37 bond0 /dev/mapper/vmstore-vm37
    vbladed 2 38 bond0 /dev/mapper/vmstore-vm38
    vbladed 2 39 bond0 /dev/mapper/vmstore-vm39
    vbladed 2 40 bond0 /dev/mapper/vmstore-vm40
    vbladed 2 41 bond0 /dev/mapper/vmstore-vm41
    vbladed 2 42 bond0 /dev/mapper/vmstore-vm42
    vbladed 2 43 bond0 /dev/mapper/vmstore-vm43
    vbladed 2 44 bond0 /dev/mapper/vmstore-vm44
    vbladed 2 45 bond0 /dev/mapper/vmstore-vm45
    vbladed 2 46 bond0 /dev/mapper/vmstore-vm46
    vbladed 2 47 bond0 /dev/mapper/vmstore-vm47
    vbladed 2 48 bond0 /dev/mapper/vmstore-vm48
    vbladed 3 49 bond0 /dev/mapper/vmstore-vm49
    vbladed 3 50 bond0 /dev/mapper/vmstore-vm50


