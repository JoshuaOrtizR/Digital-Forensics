**Hashing in FTK Imager**

**Purpose of Hashing in Forensics:**

* **Verification:** Ensure the integrity of the digital evidence.
* **Validation:** Confirm that the evidence hasn't been altered.

**Hash an Image in FTK Imager:**

1. **Create a Disk Image:**
   * Open FTK Imager.
   * Go to **File** > **Create Disk Image**.
   * Select **Physical Drive** as the source type.
   * Choose the drive you want to image.
   * Click **Next**.

![1](https://github.com/user-attachments/assets/ebfd12da-9aa2-4d9d-87fd-23e05cf9a28e)


2. **Set Image Destination and Format:**
   * Click **Add** to specify the destination folder.
   * Select **Raw (DD)** as the image format.
   * Provide details like case number, evidence number, description, examiner name, and notes.
   * Click **Next**.

![2](https://github.com/user-attachments/assets/59b5263e-6fc7-4274-b300-6c45912792a1)


3. **Configure Image Settings:**
   * Choose the destination folder for the image file.
   * Specify the image file name.
   * **Set fragmentation to 0** to avoid splitting the image into multiple files.
   * **Check the box for "Verify Image After Creation".** This will calculate the hash values.
   * Click **Finish**.

![3](https://github.com/user-attachments/assets/5daac300-dd68-4230-8c2c-9bf871bec141)

![4](https://github.com/user-attachments/assets/11bd715a-2be3-4739-b213-9189d439df69)


4. **Start the Imaging Process:**
   * FTK Imager will start creating the disk image.
   * Once the process is complete, it will display the **MD5** and **SHA-1** hash values of the image.

![5](https://github.com/user-attachments/assets/07e3c607-c1bf-4d0a-bb83-c69f744fc70e)

![6](https://github.com/user-attachments/assets/580127e4-1330-491f-a979-d69e643b87c4)

**SecAdmin Notes:**

* **Hashing Before and After Imaging:** FTK Imager calculates the hash values before and after the imaging process to ensure data integrity.
* **Hashing Other File Types:** You can also hash individual files within an image using FTK Imager's built-in hashing tools.
* **Using Other Hashing Tools:** While FTK Imager provides built-in hashing, you can also use standalone tools like `md5sum` or `sha256sum` in Linux or other hashing utilities in Windows for additional verification.
* **Consider Other Image Formats:** While DD is a popular format, explore other formats like E01 or AFF, especially for larger images or specific forensic requirements.

Common image formats used in digital forensics:

**Raw (DD):**

* **Simple and Uncompressed:** A bit-for-bit copy of the original data, without any additional metadata or compression.
* **Widely Supported:** Compatible with many forensic tools.
* **Best for Integrity:** Ensures the original data remains unaltered.
* **Can Be Large:** Due to lack of compression, raw images can be quite large.

**Smart:**

* **Proprietary Format:** Developed by Guidance Software for use with EnCase.
* **Compressed:** Can significantly reduce image size.
* **Includes Metadata:** Stores additional information about the image, such as hash values, timestamps, and user comments.
* **Limited Compatibility:** Primarily used with EnCase and other Guidance Software tools.

**E01:**

* **Standard Format:** A widely-used format, often considered the industry standard.
* **Compressed:** Supports compression, reducing image size.
* **Includes Metadata:** Stores additional information about the image, such as hash values, timestamps, and user comments.
* **Good Compatibility:** Supported by many forensic tools.

**AFF (Advanced Forensic Format):**

* **Flexible Format:** Supports various compression algorithms and metadata options.
* **Efficient:** Can be more efficient than other formats, especially for large images.
* **Good Compatibility:** Supported by many forensic tools.

**Choosing the Right Format:**

The best format for a specific case depends on several factors:

* **Storage Space:** If storage space is limited, compressed formats like Smart or E01 can be beneficial.
* **Compatibility:** Consider the tools you'll be using for analysis. Some tools may have better support for specific formats.
* **Integrity:** If preserving the exact bit-for-bit copy of the data is crucial, a raw DD image is the best choice.
* **Metadata:** If you need to store additional information about the image, E01 or AFF are good options.





