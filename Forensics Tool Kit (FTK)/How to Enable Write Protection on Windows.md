**How to Enable Write Protection on Windows:**

1. **Access Registry Editor:**
   - Press **Windows+R** to open the Run dialog.
   - Type **regedit** and press Enter.

2. **Navigate to the Registry Key:**
   - Navigate to the following key:
     ```
     HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\StorageDevicePolicies
     ```

3. **Create a New DWORD Value:**
   - Right-click on the `StorageDevicePolicies` key and select **New** > **DWORD (32-bit) Value**.
   - (Even you are using 64bit go with 32bit)
   - Name the new value **WriteProtect**.

4. **Modify the Value Data:**
   - Double-click the `WriteProtect` value.
   - Set the **Value data** to **1** (one).
   -  (1=True, 0=False)
   - Click **OK**.
   

5. **Restart Your Computer:**
   - Restart your computer for the changes to take effect.

**Verifying Write Protection:**

1. **Create a Test Folder:**
   - Create a new folder on your desktop named "Test".

2. **Attempt to Modify the Drive:**
   - Try to copy or move the "Test" folder to your USB drive.
   - If you receive a message indicating that the disk is write-protected, write protection is enabled.

![Test](https://github.com/user-attachments/assets/df9ca698-a217-4e1e-821b-e3c5e81fec65)


**SecAdmin Notes:** Disabling write protection can compromise the integrity of digital evidence. Use this method with caution and only when necessary. It's generally recommended to use physical write blockers to ensure data integrity during forensic investigations.
 
* **Hashing Evidence:** Before and after any analysis, hash the evidence to verify its integrity.
* **Chain of Custody:** Maintain a detailed record of who has accessed the evidence and when.
* **Forensic Software:** Use specialized forensic software to analyze evidence without modifying it.
* **Drive Docks and Write Blockers:** Physical devices that secure digital evidence by preventing accidental or intentional modifications.
* **Hash Value:** A unique digital fingerprint of data, used to verify data integrity.
* **Mounting:** Making a storage device accessible to the operating system.
* **Chain of Custody:** A documented, unbroken sequence of custody, control, transfer, analysis, and disposition of evidence.
