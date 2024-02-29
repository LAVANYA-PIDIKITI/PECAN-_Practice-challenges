# Love Letter
Difficulty: easy
Using Python, a student has encrypted a secret message to send to their girlfriend. The code used to encrypt the message can be found in the attached file.

With the code, he generated the following ciphertext:
[315, 324, 363, 294, 294, 363]

You were able to intercept the message, but you don’t have a way to decrypt it back into plaintext.

Figure out how to decrypt the message and determine what the secret message is

Download the python script
```python


def encryptionFunction():

    #Variables
    ciphertext = []
    ascii_values = []
    
    #Prompt to enter plaintext to be encrypted
    plaintext = input('Please enter text to be encrypted: ')

    #Each letter in the message is converted to ASCII and
    #appended to a list
    for character in plaintext:
        ascii_values.append(ord(character))

    #Each ASCII character is multiplied by 3
    for element in ascii_values:
        ciphertext.append(element * 3)

    #Ciphertext is returned
    return ciphertext


while True:
    print(encryptionFunction())
```
Developed by: Robbie Raftis
# Solution:
```python
def decryptionFunction(ciphertext):
    # Variable
    decrypted_text = ""

    # Each value in the list is divided by 3 and converted to ASCII
    for value in ciphertext:
        decrypted_value = int(value / 3)  # Divide and convert to int
        decrypted_text += chr(decrypted_value)  # Convert the result to ASCII and append

    # Decrypted text is returned
    return decrypted_text


def main():
    # Example input: [315, 324, 363, 294, 294, 363]
    example_input = [315, 324, 363, 294, 294, 363]

    # Function call with example input
    result = decryptionFunction(example_input)

    # Print the result
    print(f"Decrypted result: {result}")


if __name__ == "__main__":
    main()
```
1 ) Write a main function and call the written function<br>
2 ) Next first do /3 and then chr() to print the ASCII of the same<br>
![image](https://github.com/LAVANYA-PIDIKITI/PECAN-_Practice-challenges/assets/98797256/40fb9f37-66db-40b3-9f17-c6f81f7ae438)
