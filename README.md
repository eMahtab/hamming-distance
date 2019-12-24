# Hamming Distance

The Hamming distance between two integers is the number of positions at which the corresponding bits are different.

Given two integers x and y, calculate the Hamming distance.

Note:
0 ≤ x, y < 2^31.
```
Example:

Input: x = 1, y = 4

Output: 2

Explanation:
1   (0 0 0 1)
4   (0 1 0 0)
       ↑   ↑

The above arrows point to positions where the corresponding bits are different.
```

### Implementation

```java
public int hammingDistance(int x, int y) {
		int count = 0;
		while(x > 0 || y > 0) { // keep going as long as any one number (x or y) is greater than 0
			count += (x % 2) ^ (y % 2); // XOR between the last digits of both numbers x and y
			x = x >> 1; // same as x = x / 2;
			y = y >> 1; // same as y = y / 2;
		}
       
       return count;
}
```
