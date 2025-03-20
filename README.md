## EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## NAME : KARTHICK KISHORE T
## REG NO : 212223220042
## DATE : 20-03-2025

## AIM:

To implement the simple substitution technique named Caesar cipher using C language.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:



![image](https://github.com/Hemamanigandan/CNS/assets/149653568/eb9c6c43-8c80-4cdd-b9d4-91705a311c79)


## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.


## PROGRAM :-
```
def caesar_cipher(text, shift, mode='encrypt'):
    result = ""
    
    if mode == 'decrypt':
        shift = -shift  
    
    for char in text:
        if char.isalpha():
            shift_base = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - shift_base + shift) % 26 + shift_base)
        else:
            result += char  
    
    return result


text = input("Enter your text: ")
shift = int(input("Enter shift value: "))
mode = input("Enter mode (encrypt/decrypt): ").strip().lower()

output = caesar_cipher(text, shift, mode)
print(f"Output: {output}")
```

OUTPUT :-

# ENCRYPTION
![encrypt py](https://github.com/user-attachments/assets/835f7d9e-3a32-44f1-b70f-42ee7b6212ce)

# DECRYPTION
![decrypt py](https://github.com/user-attachments/assets/31352eda-933d-4e68-b721-d490cf2e718d)

