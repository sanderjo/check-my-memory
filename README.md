# check-my-memory
Check my memory: find hardware and OS details about RAM

Because the script uses dmidecode, you must run as root
```
sudo python3 check-my-memory.py
```
Example output:
```
$ sudo python3 check-my-memory.py 
check-my-memory.py - version: SJ 2023-08-15
OK, you're root
ANALYSIS:
Total of physical memory modules found 8 GB in 2 memory module(s)
BIOS offers 7834 MB as usable
Memory seen by OS 7578 MB
BIOS version 02/19/2021
CPU is PAE enabled
CPU is x86_64 64-bit enabled
OS is x86_64 64-bit

SUMMARY:
Memory difference between DIMM hardware and BIOS offering 357 MB
Memory difference between BIOS offering and memory seen by OS 256 MB
Memory difference between DIMM hardware and memory seen by OS 614 MB

ADVICE:
Your BIOS is not offering all of your physical memory. Try to update your BIOS, and/or enable 'memory hole remapping / hoisting' in your BIOS to get more usable memory

Finally: show more detailed memory info from lshw. This can take up to 30 seconds ...
       description: System Memory
        size: 8GiB
           description: SODIMM DDR4 Synchronous 3200 MHz (0,3 ns)
           size: 8GiB
           description: SODIMM [empty]
        description: L1 cache
        size: 96KiB
        capacity: 96KiB
        description: L1 cache
        size: 64KiB
        capacity: 64KiB
        description: L2 cache
        size: 2560KiB
        capacity: 2560KiB
        description: L3 cache
        size: 6MiB
        capacity: 6MiB
        description: RAM memory
 
Finished
```
