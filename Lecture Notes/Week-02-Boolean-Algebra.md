```
To convert a number in Excess-2^(n-1) Notation:

1. Given a string of bits called "bitString" and its length "n".

2. Ensure "bitString" is of length "n" and contains only 0s and 1s.

3. Check the first bit of "bitString":
    - If it's '1':
        - Take the remaining bits after the first bit.
        - Convert these bits directly to a decimal number. Call this "value".
    - If it's '0':
        - Add a '1' at the beginning and find the two's complement of the new bit string.
        - Convert this two's complement string to decimal. Call this "value".

4. Subtract 2^(n-1) from "value" to get the number in Excess-2^(n-1) Notation.

5. Return the result.

Example:
For "bitString" = "1010" (with n=4), in Excess-8 notation:
- Since the first bit is '1', take '010' and convert to decimal: 2.
- Subtracting the excess, 2^3 = 8, gives: 2 - 8 = -6.
So, "1010" represents -6 in Excess-8 notation.

For "bitString" = "0001" (with n=4), in Excess-8 notation:
- Since the first bit is '0', add '1' to get '10001', and find its two's complement.
- Convert this two's complement to decimal.
- Subtracting the excess, 2^3 = 8, from the converted number gives the final value.```
```

| Q | Bit pattern | 3-bit 2’s complement | excess 4 |
|---|-------------|----------------------|----------|
| 0 | `000`       | 0                    | -4       |
| 1 | `001`       | 1                    | -3       |
| 2 | `010`       | 2                    | -2       |
| 3 | `011`       | 3                    | -1       |
| 4 | `100`       | -4                   | 0        |
| 5 | `101`       | -3                   | 1        |
| 6 | `110`       | -2                   | 2        |
| 7 | `111`       | -1                   | 3        |

