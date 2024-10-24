# EX8 - ADVANCED ENCRYPTION STANDARD(AES)
## AIM :
  To Implement Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## THEORM :
The Advanced Encryption Standard (AES) is a symmetric encryption algorithm widely used to secure sensitive data. It operates on fixed block sizes of 128 bits with key lengths of 128, 192, or 256 bits. AES encrypts data through multiple rounds of substitution, permutation, and mixing to ensure confidentiality.
## ALGORITHM : 
### STEP 1 :
AES is based on a design principle known as a substitution–permutation. 
### STEP 2 :
AES does not use a Feistel network like DES, it uses variant of Rijndael. 
### STEP 3 :
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits. 
### STEP 4 :
AES operates on a 4 × 4 column-major order array of bytes, termed the state

## PROGRAM : 
```

#include <stdio.h>
#include <string.h>
void xor_encrypt_decrypt(char *input, char *key)
{
    int input_len = strlen(input);
    int key_len = strlen(key);
    for (int i = 0; i < input_len; i++) 
    {
        input[i] = input[i] ^ key[i % key_len]; 
    }
}
int main()
{
    char url[] = "https://lms2.cse.saveetha.in";
    char key[] = "secretkey"; 
    printf("Original URL: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Encrypted URL: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Decrypted URL: %s\n", url);
    return 0;
}
```
## OUTPUT :
![image](https://github.com/user-attachments/assets/aad3b476-00c1-4eff-9c41-166d70a0a2ac)

## RESULT : 
The program to implement the  Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is executed successfully.
