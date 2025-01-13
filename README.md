# Cryptography Concepts

## Overview

This project delves into cryptographic techniques such as **steganography**, **hashing operations**, and the **avalanche effect**. Utilizing tools like Steghide, CyberChef, and Linux commands, this lab demonstrates methods for secure data hiding, extraction, and the significant impact of minor input changes in cryptographic systems.

## Key Features

- **Message Embedding and Extraction**: Embed secret messages or zipped archives within image files using Steghide and Linux commands.
- **Avalanche Effect Analysis**: Investigate the effects of minor input changes on cryptographic hash outputs (e.g., MD5, SHA-1).
- **Data Integrity Verification**: Apply hashing techniques to ensure file integrity and detect changes.

## Lab Procedures

### 1. Hide a Secret Message

#### Steps:
1. Create a text file containing the secret message:
   ```bash
   echo "The password to the WinOS is NDGlabpass123!" > secret.txt
   ```
2. Embed the secret message into an image:
   ```bash
   steghide embed -cf top_secret.jpg -ef secret.txt
   ```
3. Extract the hidden message:
   ```bash
   steghide extract -sf top_secret.jpg
   ```

### 2. Hide Multiple Files in an Image

#### Steps:
1. Create a zipped archive of files to hide:
   ```bash
   zip secret_files secret.txt top_secret.jpg
   ```
2. Combine the archive with an image file:
   ```bash
   cat cyber_monday.jpg secret_files.zip > cybersec.jpg
   ```

### 3. Observe the Avalanche Effect

#### Steps:
1. Use CyberChef to hash input data with cryptographic algorithms like **MD5** or **SHA-1**.
2. Modify a single bit in the input data.
3. Compare the resulting hash values to observe the dramatic differences caused by the change.

## Tools Utilized

- **Steghide**: For embedding and extracting data within image files.
- **CyberChef**: To visualize cryptographic hash functions and analyze the avalanche effect.
- **Linux Commands**: For file manipulation, zipping, and hash computation.

## Learning Outcomes

- Master the basics of steganography for secure data hiding and extraction.
- Understand how to verify data integrity through cryptographic hashing.
- Explore the avalanche effect to appreciate the robustness of secure hash algorithms.

## Real-World Applications

- **Data Concealment**: Recognize how malicious actors might hide sensitive data in seemingly innocuous files.
- **Data Integrity**: Learn to ensure the authenticity and integrity of critical data.
- **Cryptographic Security**: Gain insight into cryptographic weaknesses and their implications for security protocols.

## Additional Resources

- [Steghide Documentation](http://steghide.sourceforge.net/documentation.php)
- [CyberChef - The Cyber Swiss Army Knife](https://gchq.github.io/CyberChef/)
- [Linux Command Reference](https://linux.die.net/man/)
- [Cryptographic Hash Functions - NIST](https://csrc.nist.gov/projects/hash-functions)

## Repository

Access project [Cryptography Concepts](https://github.com/StephVergil/Cryptography-Concepts/blob/main/Cryptography%20Concepts%20copy.docx).
