## EX. NO: 1 : IMPLEMENTATION OF CAESAR CIPHER
 

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


PROGRAM :-
```
def main():
    plain = input("\nEnter the plain text: ")
    key = int(input("Enter the key value: "))

    print("\n\tPLAIN TEXT:", plain)
    print("\n\tENCRYPTED TEXT:", end='')

    cipher = ""
    for ch in plain:
        if ch.isalpha():
            shifted = ord(ch) + key
            if ch.isupper():
                if shifted > ord('Z'):
                    shifted -= 26
            elif ch.islower():
                if shifted > ord('z'):
                    shifted -= 26
            cipher += chr(shifted)
            print(chr(shifted), end='')
        else:
            cipher += ch
            print(ch, end='')

    print("\n\n\tAFTER DECRYPTION: ", end='')

    decrypted = ""
    for ch in cipher:
        if ch.isalpha():
            shifted = ord(ch) - key
            if ch.isupper():
                if shifted < ord('A'):
                    shifted += 26
            elif ch.islower():
                if shifted < ord('a'):
                    shifted += 26
            decrypted += chr(shifted)
            print(chr(shifted), end='')
        else:
            decrypted += ch
            print(ch, end='')

if __name__ == "__main__":
    main()


```


## OUTPUT :-
![image](https://github.com/user-attachments/assets/750a07aa-e88e-426a-9287-5751f6361925)

## RESULT :-
The program is executed successfully
