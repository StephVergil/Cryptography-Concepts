# Cryptography Concepts

## Overview

This project explores cryptographic techniques such as **steganography**, **hashing operations**, and the **avalanche effect**. Using tools like Steghide, CyberChef, and basic Linux commands, the lab demonstrates secure data hiding, extraction, and the impact of small changes in cryptographic inputs.

## Key Features

- **Hiding Messages**: Embed and extract secret messages or zipped archives within image files using Steghide and Linux commands.
- **Avalanche Effect**: Explore how changing a single bit in input data affects cryptographic hash outputs (MD5/SHA-1).
- **File Security**: Learn methods to verify data integrity using hash values.

## Lab Steps

1. **Hide a Secret Message**:
   - Create a text file:
     ```bash
     echo “The password to the WinOS is NDGlabpass123\!” > secret.txt
     ```
   - Embed the message in an image:
     ```bash
     steghide embed -cf top_secret.jpg -ef secret.txt
     ```
   - Extract the hidden message:
     ```bash
     steghide extract -sf top_secret.jpg
     ```

2. **Hide Multiple Files in an Image**:
   - Create a zipped archive:
     ```bash
     zip secret_files secret.txt top_secret.jpg
     ```
   - Combine it with an image:
     ```bash
     cat cyber_monday.jpg secret_files.zip > cybersec.jpg
     ```

3. **Observe the Avalanche Effect**:
   - Use CyberChef to hash input data with **MD5** or **SHA-1**.
   - Modify a single bit and compare the resulting hash to observe significant differences.

## Tools Used

- **Steghide**: For embedding/extracting data within images.
- **CyberChef**: To visualize cryptographic hash functions and the avalanche effect.
- **Linux Commands**: For file management, zipping, and hash verification.

## Key Learning Objectives

- Understand steganography techniques to hide and extract data.
- Verify data integrity with hash functions before and after embedding operations.
- Explore the importance of strong randomization in secure cryptographic algorithms.

## Real-World Applications

- Learn how attackers hide data in innocuous files and how to detect it.
- Understand the significance of cryptographic integrity checks.
- Observe cryptographic weaknesses through practical experimentation.

## Documentation

For full instructions, refer to the [Cryptography Lab Guide](https://github.com/StephVergil/Cybersecurity-Projects/blob/main/Cryptography%20Concepts%20copy.docx).
