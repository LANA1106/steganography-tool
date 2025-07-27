# Steganography Tool

**Project Completed By**: Rajveer Solanki  
**Date**: July 24, 2025  
**Status**: READY FOR SUBMISSION ✅

## Overview
This Steganography Tool is a Python application that allows users to securely hide and retrieve text or files within images using the Least Significant Bit (LSB) method. The tool features a user-friendly GUI built with Tkinter and optional encryption for added security.

## Features
- **Text & File Hiding:** Embed text or files in PNG/BMP images
- **Extraction:** Retrieve hidden messages or files from images
- **Encryption:** Optional password-based encryption to secure hidden data
- **User Interface:** Intuitive Tkinter GUI with drag-and-drop support

## Installation
1. **Clone the repository:**
   ```bash
   git clone https://github.com/LANA1106/steganography-tool.git
   cd steganography-tool
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. **Run the application:**
   ```bash
   python main.py
   ```
2. **Follow GUI instructions:**
   - Select image for encoding/decoding
   - Enter message/file to hide/extract
   - Use password for encryption if desired

## Project Structure
```
.
├── main.py              # Entry point
├── steg.py              # Steganography algorithms
├── gui.py               # GUI implementation
├── requirements.txt     # Dependencies
├── README.md            # Project documentation
└── .gitignore          # Git ignore rules
```

## Technical Details

### Steganography Method
- **Algorithm:** Least Significant Bit (LSB) modification
- **Image Formats:** PNG, BMP (lossless formats)
- **Capacity:** Approximately (width × height × 3) ÷ 8 bytes per image
- **Data Integrity:** Null-terminator marking for reliable extraction

### Encryption
- **Algorithm:** Fernet symmetric encryption (AES 128)
- **Key Derivation:** Password-based with 32-byte key padding
- **Encoding:** Base64 for safe text representation

### Dependencies
- **Pillow (PIL):** Image processing and manipulation
- **cryptography:** Encryption/decryption functionality
- **tkinter:** GUI framework (included with Python)

## Requirements
- Python 3.6 or higher
- Windows, macOS, or Linux
- Required packages listed in `requirements.txt`

## Example Usage

### Hiding Text
1. Select a PNG or BMP image
2. Enter your secret message
3. Optional: Set a password for encryption
4. Click "Encode Message" and save the output image

### Extracting Text
1. Select the image containing hidden data
2. Optional: Enter the password if encrypted
3. Click "Decode Message" to reveal the hidden text

### File Operations
- Use "Browse File" to select any file type for hiding
- Extract files will preserve original filename and format
- Encrypted files are prefixed with "enc_" in the filename

## Security Notes
⚠️ **Important:** This tool is designed for educational and basic privacy purposes. For production security applications, consider:
- Using stronger key derivation functions (PBKDF2, Argon2)
- Adding salt to password-based encryption
- Implementing steganographic analysis resistance

## Troubleshooting

### Common Issues
- **"Decryption failed"**: Check password or verify the image contains encrypted data
- **File too large**: Ensure the file size doesn't exceed image capacity
- **Unsupported format**: Use PNG or BMP images only

## License
This project is licensed under the MIT License - see the LICENSE file for details.
 
