Simple BitToHex conversion tool

This tool is used to convert coin flip entropy to HEX format commonly used in the crypto wallets.
User should flip 8 coins multiple times until enough entropy is collected.
Than use that entropy in HEX format to create master seed.
Master seed can than be used in any hardware or software wallet.

How to verify that this tool does not affect the entropy (does not have a backdoor).

1. Read the source code. It is short
2. Use any tool to create SHA256 hash. i.e. `6b86b273ff34fce19d6b804eff5a3f5747ada4eaa22f1d49c01e52ddb7875b4b`
3. Use any external tool to convert this HEX string to binary i.e. `0110101110000110101100100111001111111111001101001111110011100001100111010110101110000000010011101111111101011010001111110101011101000111101011011010010011101010101000100010111100011101010010011100000000011110010100101101110110110111100001110101101101001011`

   **Note:** Some online tools do not work with big numbers, and may return too many zeroes at the end. Some truncate zeroes at the start. Do not use them.

4. Input the resulting binary string into **this** tool. You should get back the original HEX string.
5. That means that the tool is indeed just a bin to hex converter

6. You **HAVE TO VERIFY** because it is very easy to add backdoor to this tool! The backdoor will reduce the entropy and it would be trivial to brute-force the seed on the hacker's side.
