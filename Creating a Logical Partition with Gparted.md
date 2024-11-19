**Creating a Partition with GParted on a VM**

**Tools:**
* Windows Computer
* VM (Debian ISO Image)
* GParted

**Steps:**

 **Set Up the VM:** Create a virtual machine using your preferred virtualization software (e.g., VirtualBox, VMware). Install the Debian ISO image onto the VM.
 **Launch GParted:** Open GParted on your Windows computer.
 ![Step1](https://
github.com
/user-attachments/assets/6e5dc87f-b0c3-483b-b960-6e1bbf47b74c)

**Identify the Drive:** Locate the drive corresponding to your VM. You can identify it by its size.
![Step2](https://
github.com
/user-attachments/assets/caf60725-1436-4956-8a29-b344e87011f6)
![Step3](https://
github.com
/user-attachments/assets/af575cc8-053c-4977-8f9d-84802727e744)

**Resize the Partition:** Resize the existing partition to create unallocated space for the new partition.
![Step4](https://
github.com
/user-attachments/assets/390f440f-8fc4-4f04-b759-a00c1f813682)

![Step5](https://
github.com
/user-attachments/assets/bcf16833-4337-4776-96b3-4d54bca4ce26)

**Create a New Partition:** Create a new logical partition in the unallocated space.
**Format the Partition:** Format the new partition with the ext4 file system.
![6](https://
github.com
/user-attachments/assets/f8876923-d9ed-4dc5-8c2a-98ec5d546d2b)
![7](https://
github.com
/user-attachments/assets/64100950-9070-4917-9668-8f5cdbdf1bc0)

Finally, to save your changes, click on the green checkmark. Remember to format the file system as FAT32.
![FinalStep](https://
github.com
/user-attachments/assets/131c59c0-39d7-4f8c-95b3-64e99233d5c1)


**SecAdmin Notes:**

* **Data Preservation:** Always create a copy of the data before making any changes. This is especially crucial in forensic investigations.
* **Live Acquisition:** Consider using a live Linux distribution on a USB drive to perform data acquisition directly from the device.
* **Sector-Level Understanding:** Each sector typically stores 512 bytes of data. Sectors are used for addressing purposes.
* **MBR Record:** The Master Boot Record (MBR) is located in the first sector of the device.
* **Device and Partition Naming:** Refer to devices (e.g., USB drives) using device names like `/dev/sdb` and partitions using partition names like `/dev/sda5`.


**File Systems:**

* **FAT (File Allocation Table):** An older file system that is simple and widely supported. It is often used for older devices and storage media like floppy disks and USB drives.
* **NTFS (New Technology File System):** A more advanced file system developed by Microsoft. It offers features like security permissions, compression, and large file support. It is commonly used on Windows systems.

**Memory:**

* **RAM (Random Access Memory):** Volatile memory that stores data temporarily while a computer is running. It is used for active programs and data.

**Telecommunications and Security:**

* **SIM (Subscriber Identity Module):** A small, removable chip that stores information about a mobile phone subscriber, such as their phone number and network settings.
* **SMTP (Simple Mail Transfer Protocol):** A protocol used to send and receive email messages.
* **ACE (Access Control Entry):** A security setting that defines permissions for users or groups to access resources on a computer system.

**Tools and Hardware:**

* **Hex Editors:** Tools used to view and edit files at the binary level. They are often used for reverse engineering, data recovery, and security analysis.
* **CMOS (Complementary Metal-Oxide Semiconductor):** A type of transistor used in electronic circuits. It is the fundamental building block of modern digital electronics.
* **BIOS (Basic Input/Output System):** Firmware that initializes hardware components when a computer is turned on. It is responsible for tasks like detecting and configuring devices, running diagnostic tests, and loading the operating system.





