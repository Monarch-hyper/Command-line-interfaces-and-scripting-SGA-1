# Storage Health Assessment

## Objective

The objective of this task is to inspect the Linux storage devices, mounted filesystems, disk utilization, and inode usage using standard Linux commands.

---

## Commands Used

### `lsblk`

Displays all available block storage devices and their mount points.

The output confirms the primary storage device **sda** with the mounted root partition **/dev/sda1**.

---

### `df -h`

Displays filesystem disk usage in a human-readable format.

The output shows that the root filesystem is using approximately **23%** of the available disk space.

---

### `df -i`

Displays inode usage for each mounted filesystem.

The root filesystem is utilizing approximately **10%** of the available inodes, indicating healthy inode availability.

---

## Conclusion

The storage assessment confirms that the primary storage device is functioning correctly. Disk utilization remains low, inode usage is within normal limits, and all required filesystems are properly mounted. Overall, the system storage is healthy and has sufficient free capacity.
