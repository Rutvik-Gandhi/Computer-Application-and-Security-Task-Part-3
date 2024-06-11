# Computer-Application-and-Security-Task-Part-3

# File Encryption and Decryption Guide using OpenSSL

This guide provides step-by-step instructions for encrypting and decrypting a file using OpenSSL in Kali Linux.

## Encryption Process

1. **Encrypt the File:**
   - Open a terminal in Kali Linux.
   - Use the following command to encrypt the file `yourFirstName.txt` using AES-256-CBC encryption:
     ```
     openssl enc -aes-256-cbc -in yourFirstName.txt -out encrypted1.bin
     ```
   Replace `yourFirstName.txt` with the actual filename if it's different.

2. **View Plain-Text Contents of the File:**
   - Issue the following command to display the plain-text contents of the file:
     ```
     cat yourFirstName.txt
     ```

3. **Repeat Encryption with Base64 Encoding:**
   - Repeat the encryption process, but this time include the `-base64` option:
     ```
     openssl enc -aes-256-cbc -in yourFirstName.txt -out encrypted2.bin -base64
     ```

4. **View Encrypted Contents:**
   - Issue the following command to view the contents of the encrypted file:
     ```
     cat encrypted2.bin
     ```

## Decryption Process

1. **Decrypt the Encrypted File:**
   - To decrypt the encrypted file (`encrypted.bin`), use the appropriate command option within the OpenSSL tool:
     ```
     openssl enc -d -aes-256-cbc -in encrypted1.bin -out decrypted1.txt
     ```
   This command decrypts `encrypted1.bin` and saves the decrypted content in `decrypted1.txt`.

2. **Verify Decrypted Content:**
   - Verify the decrypted content by opening `decrypted1.txt` to ensure it matches the original plain-text content of `yourFirstName.txt`.

## Disclaimer

This guide is for educational purposes only. Ensure that you have proper authorization before encrypting or decrypting any files.
