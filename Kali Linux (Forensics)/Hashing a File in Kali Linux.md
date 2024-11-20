**Hashing a File in Kali Linux**

**Create a File:**
   * Open a terminal.
   * Use the `touch` command to create a new file:
     ```bash
     touch test.txt
     ```
![1](https://github.com/
user-attachments/assets/8142c32a-f7c8-4150-bcf7-b3334af91595)

**Edit the File:**
   * Use a text editor like `vim` to add content:
     ```bash
     vim test.txt
     ```
     * Press `i` to enter insert mode.
     * Type your desired text.
     * Press `Esc` to exit insert mode.
     * Type `:wq` to save and quit the editor.

![2](https://github.com/
user-attachments/assets/1000f458-147c-4812-b8fd-8b75de52d679)

**Calculate the Hash:**
   * Use the `sha256sum` command to calculate the SHA-256 hash:
     ```bash
     sha256sum test.txt
     ```
     * This will output a 64-character hexadecimal hash value.

![3](https://github.com/
user-attachments/assets/e71aff23-687b-4570-b208-06fd5b96f1fa)
**Experimenting with File Name and Hash:**

To test if changing the file name affects the hash, you can:
**Rename the File:**
   * Use the `mv` command to rename the file:
     ```bash
     mv test.txt new_test.txt
     ```
**Calculate the Hash Again:**
   * Use the `sha256sum` command on the new file name:
     ```bash
     sha256sum new_test.txt
     ```
   * Compare the new hash with the original one.

**SecAdmin Notes:**

* **Hash Sensitivity to Content:** The hash value is highly sensitive to the content of the file. Even a small change in the file's content will result in a completely different hash.
* **Hash Independence from File Name:** The hash value is independent of the file name. Renaming a file does not change its hash as long as the content remains the same.

