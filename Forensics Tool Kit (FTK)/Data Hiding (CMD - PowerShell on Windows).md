**Data Hiding**

Data hiding is a technique used to conceal sensitive information within another file, making it invisible to casual observation. This can be achieved by leveraging the Alternate Data Stream (ADS) feature of Windows. 


1. **Create an Empty File:**
   * Open a command prompt.
   * Type the following command and press Enter:
     ```
     type nul > ADS.txt
     ```
   * This creates an empty file named "ADS.txt".

![1](https://github.com/user-attachments/assets/5ea976d0-faf0-42d3-960a-317644fbc5f1)

2. **Add a Hidden Data Stream:**
   * In the same command prompt, type the following command and press Enter:
     ```
     echo "Secret Data" > ADS.txt:secret
     ```
   * This adds a hidden data stream named "secret" to the "ADS.txt" file. The content "Secret Data" will be stored within this hidden stream.

![2](https://github.com/user-attachments/assets/dda3f173-16d7-48c2-9e43-d78fece7a0c7)

3. **Verify the Hidden Data Stream:**
   * Open PowerShell.
   * Type the following command and press Enter:
     ```
     get-item ADS.txt -stream *
     ```
   * This command will list all data streams associated with the "ADS.txt" file, including the hidden "secret" stream.

![3](https://github.com/user-attachments/assets/df74db0f-c218-4135-905c-18ceb7aa5b4b)

![4](https://github.com/user-attachments/assets/a8d28081-194b-4cb7-88a8-5e1e742780e3)

4. **View the Contents of the Hidden Data Stream:**
   * In PowerShell, type the following command and press Enter:
     ```
     get-content ADS.txt -stream secret
     ```
   * This will display the contents of the "secret" data stream, which is "Secret Data" in this case.

![5](https://github.com/user-attachments/assets/5065a7d5-571e-4931-9343-b51bbbeebaf8)


**Hiding Executable Files:**
You can also hide executable files within an ADS. This can be dangerous if malicious actors exploit this technique to conceal harmful programs. 

* **Hide an Executable:**
  ```
  type C:\Windows\System32\notepad.exe > ADS.txt:note
  ```
  This command hides the Notepad executable within the "note" data stream of the "ADS.txt" file.

![Last](https://github.com/user-attachments/assets/ca76c66a-0750-41fc-9e8d-eb376325eda5)

**Sec Admin Notes:**
* **Invisibility:** The hidden data stream is not visible in standard file explorers.
* **Potential Abuse:** Malicious actors can use ADS to hide malware or other harmful files.
* **Malware Detection:** Use robust antivirus and anti-malware software to detect and remove threats.

