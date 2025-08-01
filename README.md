# PRODIGY_CS_01 - Caesar Cipher Encryption & Decryption 🔐

## 📌 Task Objective
Create a Python program to:
- Encrypt and decrypt text using the Caesar Cipher algorithm
- Allow the user to input a message and shift value

## 🖥 Technologies Used
- Python 3

## 🧪 How It Works
1. User enters a message
2. User provides a shift number (e.g., 3)
3. The program encrypts the message by shifting letters
4. The program then decrypts it back to the original

## 📷 Screenshots
Main Code:
def encrypt(text, shift):
    result = ""
    for char in text:
        if char.isupper():
            result += chr((ord(char) + shift - 65) % 26 + 65)
        elif char.islower():
            result += chr((ord(char) + shift - 97) % 26 + 97)
        else:
            result += char
    return result

def decrypt(text, shift):
    return encrypt(text, -shift)

# User input
message = input("Enter the message: ")
shift = int(input("Enter shift value (e.g., 3): "))

encrypted = encrypt(message, shift)
print("Encrypted message:", encrypted)

decrypted = decrypt(encrypted, shift)
print("Decrypted message:", decrypted)

Output:
# Example to demonstrate
message = "HelloWorld"
shift = 3

encrypted = encrypt(message, shift)
decrypted = decrypt(encrypted, shift)

print("Original Message :", message)
print("Shift Value      :", shift)
print("Encrypted Message:", encrypted)
print("Decrypted Message:", decrypted)
![Caesar Cipher Output]<img width="933" height="132" alt="ex1" src="https://github.com/user-attachments/assets/6fae5b87-98af-489d-abbc-5c047ae3d0c7" />
![Caesar Cipher Output]<img width="904" height="114" alt="ex2" src="https://github.com/user-attachments/assets/c59a5eea-a54a-43b5-a1b7-e7906f7c1e86" />

## 📁 Files Included
- `caesar_cipher.py` – Main Python file
- `README.md` – This file
- `screenshots/` – Folder containing images of program output

## 👩‍🎓 Intern Details
- Name: Avishka Garud
- Internship Track: Cybersecurity
- Task No: 01
- Date: 1st August 2025
