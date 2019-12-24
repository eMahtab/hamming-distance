# Hamming Distance

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
