# Using-tools-like-John-the-Ripper-for-password-cracking
## AIM:
To crack password hashes using John the Ripper in Kali Linux.

## DESIGN STEPS:
### Step 1:
Install John the Ripper using the command:

### Step 2:
Prepare the password hash file (e.g., using unshadow for Linux password and shadow files).


### Step 3:
Use John the Ripper to crack the hashes:

## PROGRAM:
Install the John Ripper:
```
sudo apt install john
```
Create a Password-Protected ZIP File Archive a normal file (secret.txt) into a password-protected ZIP file:
```
zip --password 123abc secret.txt.zip secret.txt
```
Extract the Hash from the ZIP File:
```
zip2john secret.txt.zip > zip_hash.txt
```
Crack the ZIP Password using John:
```
john --format=zip zip_hash.txt
```
Show the Cracked Password:
```
john --show zip_hash.txt
```

## OUTPUT:
Cracked Passwords from Hash File
![image](https://github.com/user-attachments/assets/a28e901a-37e6-41b9-b1a0-ad84bd105f93)

![image](https://github.com/user-attachments/assets/01e7d1bd-ad8b-412f-966e-b2c558757fbb)

Generate Hash Using zip2john:

![image](https://github.com/user-attachments/assets/343a6cb6-a65c-4f5b-9eae-d46e12b4b890)


![image](https://github.com/user-attachments/assets/904e9bf0-d9a3-42b9-af7c-d7216f1e2750)


![image](https://github.com/user-attachments/assets/53822584-f288-47b7-93a6-b18d04c4cd8e)

## RESULT:
The password hashes were successfully cracked using John the Ripper.

