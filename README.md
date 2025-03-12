# Registry Persistence Script

##  Overview
This script demonstrates how to achieve persistence on a Windows system by adding an executable file to the Windows Registry. Additionally, it attempts to open a file from a temporary directory and repeatedly prints a specific message on the screen.

##  Features
- Copies itself to the **AppData** directory.
- **Adds an entry to the Registry** to run automatically at system startup.
- Attempts to open a file (`nota.pdf`) from the **`_MEIPASS`** directory.
- **Prints a specific message** with a delay.

##  How It Works
1. **Persistence Mechanism:**
   - The script copies itself as `AppData\sysupgrades.exe` if it does not already exist.
   - Then, it adds an entry under `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run`, ensuring it runs every time the system starts.

2. **File Execution:**
   - It tries to open a file named `nota.pdf` in the `_MEIPASS` directory, which is commonly used by PyInstaller-packaged applications.

3. **Looped Message Display:**
   - Runs a **loop 100 times**, printing the message **"i hack you :)"** every **0.5 seconds**.

##  Security & Ethical Considerations
This script exhibits behaviors commonly found in malware, including:
- **Modifying the Windows Registry to maintain persistence.**
- **Executing files without user consent.**
- **Displaying disruptive messages on the system.**

⚠ **Warning:** Running this script on a system may be flagged as malicious by security software. Ensure you fully understand its effects before executing it.

##  Possible Use Cases
- **Educational Purposes:** Learning Windows persistence techniques.
- **Malware Analysis:** Studying how malicious programs remain active on a system.
- **Security Testing:** Evaluating if antivirus or endpoint protection software detects and mitigates such behavior.

##  Legal Disclaimer
This script is provided for **educational and research purposes only**. Any misuse of this script for unauthorized access or malicious activity is strictly prohibited.

---
