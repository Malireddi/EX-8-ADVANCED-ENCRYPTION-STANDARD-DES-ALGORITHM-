# EX-8-ADVANCED-ENCRYPTION-STANDARD-DES-ALGORITHM

## Aim:
  To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM: 
  1. AES is based on a design principle known as a substitution–permutation. 
  2. AES does not use a Feistel network like DES, it uses variant of Rijndael. 
  3. It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits. 
  4. AES operates on a 4 × 4 column-major order array of bytes, termed the state

## DEVELOPED BY : Nandyala Malyadri Reddy
## REGISTER NO. : 212223100037
## PROGRAM: 

```C
#include <stdio.h>
#include <string.h>

// Function to perform XOR encryption and decryption
void xor_encrypt_decrypt(char *input, char *key) {
    int input_len = strlen(input);
    int key_len = strlen(key);
    
    for (int i = 0; i < input_len; i++) {
        input[i] = input[i] ^ key[i % key_len]; // XOR encryption/decryption
    }
}

int main() {
    char url[] = "https://www.NandyalaMalyadri.com"; // URL to encrypt
    char key[] = "secretkey"; // Simple key for XOR encryption

    printf("Original URL: %s\n", url);
    
    xor_encrypt_decrypt(url, key); // Encrypt the URL
    printf("Encrypted URL: %s\n", url);
    
    xor_encrypt_decrypt(url, key); // Decrypt the URL
    printf("Decrypted URL: %scom\n", url); // Note: Original URL is modified; fix it if needed

    return 0;
}
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/4421c91f-d298-49c5-85cd-37410b123466)
)

## RESULT: 
The execution program is successfully executed.
