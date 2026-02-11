# Tools you will need
- https://rot13.com/
- Basic text editor (Word, Notepad or LibreOffice (For the Linux folks))

## What is ROT13
- ROT13 is a simple letter substitution cipher that replaces a latter with the 13th letter in the Latin alphabet.
	- Example being:
		- A = N
		- B = O
		- and so forth
Since there are only 26 letter in the basic Latin alphabet you can also use the ROT13 inverse equation
$$
ROT_{13} (ROT_{13}(x)) = x
$$
## Simple Input and Output of ROT13

| Input  | ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz |
| ------ | ---------------------------------------------------- |
| Output | NOPQRSTUVWXYZABCDEFGHIJKLMnopqrstuvwxyzabcdefghijklm |
Notice how in the input "ABCD" are as normal but in the output they are "NOPQ" as the letters have shifted 13 characters in the Latin alphabet.

# How to solve the 'Mod 26' CTF
## Description:
- Cryptography can be easy, do you know what ROT13 is?
	- File Download for "values.txt"

## What is contained within the 'values.txt' file?
- **Contents**:
	- "cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_45559noq}"

## Solving the challange
- Open the 'values.txt' file
- Copy the garbled text
- Open your web browser and go to https://rot13.com/
- Paste the garbled text in the top box (DO NOT CHANGE THE MIDDLE OPTION OFF 'ROT13')
- Congratulations you have your flag! Go back to PicoCTF paste it in the box and click 'Submit'