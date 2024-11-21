
**Exploring a FAT File System**

* **Partitioning:** To create partitions on a storage device, tools like GParted are commonly used. This involves dividing the disk into smaller sections, each with its own file system.
* **Master Boot Record (MBR):** The MBR, located in the first sector of a disk, contains information about the partitions on the disk, including their size, location, and file system type.
* **Partition Boot Sector (PBS):** Each partition has its own PBS, which contains information about the file system within that partition.

**Using TSK to Investigate a File System**

**1. Identifying Partitions with MMLS:**
   * **Open a Terminal:** Launch a terminal window on your system.
   * **Run the MMLS Command:** Type the following command and press Enter:
     ```bash
     mmls /dev/sdb
     ```
   * **Interpret the Output:** The output will display information about the partition table on the device `/dev/sdb`. You'll see details like partition numbers, start and end sectors, and file system types (e.g., FAT32, NTFS).

**2. Listing Files and Directories with FLS:**
   * **Run the FLS Command:** Type the following command to list files and directories within a specific partition:
     ```bash
     fls /dev/sdb1
     ```
     Replace `sdb1` with the appropriate partition number if you want to examine a different partition.
   * **Understand the Output:** The output will list files and directories, along with their attributes:
     * **Regular Files:** `r/r`
     * **Directories:** `d/d`
     * **TSK Virtual Files and Directories:** `v/v`

![1](https://github.com/user-attachments/assets/9346e98c-5be2-49eb-9150-23a61e1d1dc2)

**SecAdmin Notes:**

* **Evidence Recovery:** Understanding file systems and partition structures for recovering deleted files and other digital evidence.
* **Investigating Malicious Activity:** By analyzing file system metadata and file contents, digital forensics experts can uncover evidence of cyberattacks, data breaches, and other malicious activities.
* **Data Recovery:** In cases of data loss, knowledge of file systems can help recover valuable data.

