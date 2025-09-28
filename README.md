# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM

# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.

AES does not use a Feistel network like DES, it uses variant of Rijndael.

It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.

AES operates on a 4 × 4 column-major order array of bytes, termed the state

# PROGRAM:

```
#include <stdio.h>
#include <string.h>

int main() {
    char text[100], key[100], enc[100], dec[100];
    int i;
    
    printf("Enter the plaintext: ");
    scanf("%s", text);
    printf("Enter the key: ");
    scanf("%s", key);

    // Encryption
    for (i = 0; i < strlen(text); i++)
        enc[i] = text[i] ^ key[i % strlen(key)];
    enc[i] = '\0';

    // Print ASCII values
    printf("Encrypted Message (ASCII values): ");
    for (i = 0; i < strlen(enc); i++)
        printf("%d ", (unsigned char)enc[i]);
    printf("\n");

    // Decryption
    for (i = 0; i < strlen(enc); i++)
        dec[i] = enc[i] ^ key[i % strlen(key)];
    dec[i] = '\0';

    printf("Decrypted Message: %s\n", dec);

    return 0;
}

```
# OUTPUT:


<img width="1707" height="1028" alt="Screenshot 2025-09-28 172906" src="https://github.com/user-attachments/assets/a3e7ae5d-1843-4206-84c7-4fcdf5168214" />


# RESULT:

 Using Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption was successful.....

