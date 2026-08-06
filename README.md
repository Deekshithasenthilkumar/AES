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

int main()
{
    char url[100], key[20];
    int i, keylen;

    printf("Enter URL: ");
    scanf("%s", url);

    printf("Enter Key: ");
    scanf("%s", key);

    keylen = strlen(key);

    // Encryption
    for(i = 0; url[i] != '\0'; i++)
    {
        url[i] = url[i] ^ key[i % keylen];
    }

    printf("\nEncrypted URL: ");
    for(i = 0; i < strlen(url); i++)
    {
        printf("%02X", (unsigned char)url[i]);
    }

    return 0;
}
```

# OUTPUT:
<img width="613" height="230" alt="WhatsApp Image 2026-08-06 at 9 16 57 AM" src="https://github.com/user-attachments/assets/e91788b2-cc20-4f18-951f-300170f199fd" />



# RESULT:
Thus , the AES-based URL encryption concept was implemented successfully using C, and the encrypted URL was obtained.

