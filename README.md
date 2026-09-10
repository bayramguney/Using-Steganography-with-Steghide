# Using-Steganography-with-Steghide

# Lab - Using Steganography with Steghide

## Overview
This lab demonstrates how to use **Steghide** to hide a confidential document inside a JPEG image using steganography. The hidden file was encrypted with a passphrase, verified, and successfully extracted.

## Objectives
- Hide a file inside an image.
- Encrypt the hidden file with a passphrase.
- Verify the embedded data.
- Extract the hidden file.

## Tools Used
- Ubuntu Linux
- Steghide
- LibreOffice Writer
- Terminal

## Commands Used

```bash
libreoffice secret.odt &
steghide embed -cf keyboard.jpg -ef secret.odt
steghide info keyboard.jpg
steghide extract -sf keyboard.jpg
```

## Procedure
1. Opened the secret document and the carrier image.
2. Embedded `secret.odt` into `keyboard.jpg` using `steghide embed`.
3. Entered a passphrase to encrypt the hidden file.
4. Verified the embedded data using `steghide info`, which confirmed the embedded file, Rijndael-128 (AES) encryption, CBC mode, and compression.
5. Extracted the hidden file using `steghide extract` and entered the correct passphrase.
6. Successfully recovered `secret.odt`.

## Results
The secret document was successfully hidden inside the JPEG image, encrypted, verified, and extracted without any data loss. This lab demonstrates how steganography and encryption can be used together to securely conceal sensitive information within digital media.
