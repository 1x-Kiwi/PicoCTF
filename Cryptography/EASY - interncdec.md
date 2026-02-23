# Tools you will need
- Text editor
- https://www.base64decode.org/
- https://www.dcode.fr/caesar-cipher
# What is a 'Caesar Cipher'
- A 'Caesar Cipher' is a simple substitution cipher where each letter in the English alphabet is shifted a fixed number of positions down.
#### How it works
- Choose a shift number 1 through 25
- Replace each letter with the latter that many positions ahead
- A example with a '3' shift: A->D, B->E,C->F, etc.
- So with a 3 shift: "HELLO" becomes 'KHOOR'
## How to identify a 'Caesar Cipher'
- **Key clues and identifiers:**
	- **Preserved letter frequencies** - Most common letters are "E, T, A" map to other common letters just shifted.
	- **Simple shift pattern** - Every letter is shifted by the same amount.
	- **No complex patterns** - Unlike more sophisticated ciphers, there are no keyword patterns or transpositions.
- **Quick identification methods:**
	- Look for common short words example being: "the" shifted to "wkh" with a 3 shift
	- Check if a constant difference exists between plaintext and ciphertext letters
	- Try to find a pattern where a frequent ciphertext letter (like "x") likely represents a common plaintext letter (like "e")

# How to solve 'interndec'
- Download the file from the PicoCTF challange and open it
- We are greeted with the following string `YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6ZzJhMnd6TW1zeWZRPT0nCg==`
- The string appears to be in Base64 so open a new tab to a Base64 decoder of your choice and input the string.
- The result should look something like this: `b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg2a2wzMmsyfQ=='`
- The result still looks like it is still encoded in Base64. We will remove `b''` and do it again.
- Once we have done that the result should look something like this: `wpjvJAM{jhlzhy_k3jy9wa3k_86kl32k2}`
- Now we have something that looks like a flag but is a garbled mess, this is what is a 'Caesar Cipher' (refer to the section above on how to identify a 'Caesar Cipher' and some information about it).
- Take that garbled mess and open a new tab to a 'Caesar Cipher' decoder and input the garbled string.
- Once decoded your result should look like this: `picoCTF{caesar_d3cr9pt3d_86de32d2}` which is our flag!
- Copy the result and paste it into PicoCTF and click submit!