# The Negotiator

**The Negotiator** is an advanced C# application designed to perform file encryption, decryption, and various remote administrative tasks through Discord. The project leverages AES-256 encryption for file security and utilizes Discord's API for remote communication and control. 

## Features

- **AES-256 Encryption/Decryption**: Securely encrypt and decrypt files or entire directories.
- **Discord Bot Integration**: Issue commands through Discord to control the application remotely.
- **File Punishment**: Delete a specific number of encrypted files remotely as a penalty.
- **Remote Screenshot**: Capture and send screenshots of the victim’s screen.
- **File Download**: Download any file from the victim's system to Discord.
- **Process Listing**: Retrieve a list of running processes on the victim's machine.
- **Install Persistence**: Install persistence in the system to ensure the application runs on startup.
- **Reboot and Shutdown**: Remotely reboot or shut down the victim's machine.
- **Directory and File Listing**: List all files in a specified directory and filter by file extension.

## Discord Commands

- `/encrypt <path>`: Encrypt all files in the specified directory.
- `/decrypt <path>`: Decrypt all files in the specified directory.
- `/punish <files>`: Delete the specified number of encrypted files.
- `/show_form`: Display the GUI form of The Negotiator.
- `/hide_form`: Hide the GUI form of The Negotiator.
- `/screenshot`: Capture and upload a screenshot of the victim's screen.
- `/download <path>`: Download a specified file from the victim’s system.
- `/list_files <path> <filetype>`: List files of a specified type from a directory.
- `/install_persistence`: Install persistence to ensure the application starts with the system.
- `/reboot`: Reboot the victim's machine.
- `/shutdown`: Shut down the victim's machine.
- `/list_processes <process_name>`: List all running processes (or filtered by name).

## Getting Started

### Prerequisites

- .NET Framework 8.0+
- Discord Bot Token
- Administrator privileges on the target system.

### Running the Discord Bot
Ensure the bot has the following intents and permissions in your Discord server:
* Send Messages
* Manage Channels
* Administrator Permissions

### Encryption Details
* Algorithm: AES-256 with CBC mode.
* Key Size: 256-bit key generated in Base64 format.
* Initialization Vector (IV): A static 16-byte zeroed IV (suitable for demonstration).

### Persistence
The Negotiator can install itself in the Windows Registry to ensure it runs at startup. It modifies the Winlogon shell registry key to execute the application alongside the Windows shell.

### Disclaimer
This software is for educational purposes only. Use it responsibly and only in environments where you have explicit permission.
