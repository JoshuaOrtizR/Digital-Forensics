**Static Acquisition**

To create an image of a USB drive using the `dd` command, follow these steps:

1. **Open a Terminal:**
   * Open a terminal window on your Linux system.

2. **Identify the USB Drive:**
   * Use the `lsblk` command to identify the device name of your USB drive. 
   * For example, it might be `/dev/sdb`.

3. **Create the Image:**
   * Type the following command, replacing `/dev/sdb` with the actual device name of your USB drive:

   ```bash
   sudo dd if=/dev/sdb of=usb_image.img bs=4M conv=sync,noerror
   ```
![1](https://github.com/user-attachments/assets/5ed99fce-a859-41fa-b9be-a69804988a60)

   * **Explanation of the command:**
     - `sudo`: Executes the command with root privileges.
     - `dd`: The command to copy and convert data.
     - `if=/dev/sdb`: Specifies the input file (the USB drive).
     - `of=usb_image.img`: Specifies the output file (the image file).
     - `bs=4M`: Sets the block size to 4 megabytes, improving performance.
     - `conv=sync,noerror`: Ensures data integrity and prevents errors from stopping the process.

![2](https://github.com/user-attachments/assets/894d030e-166b-470e-bd55-454f3eb8658c)

4. **Monitor the Process:**
   * The imaging process may take some time.
   * You can monitor the progress by checking the file size of `usb_image.img` using the `ls -lh` command.

**SecAdmin Notes:**

* **Verify the Image:**
  * Use a hash function like SHA-256 to calculate the hash of both the original drive and the image.
  * Compare the hashes to ensure data integrity.
* **Consider Using a Forensic Tool:**
  * For more advanced forensic analysis, consider using tools like `dcfldd` or `Autopsy`.
* **Backup the Image:**
  * Store the image in a secure location to preserve the evidence.

