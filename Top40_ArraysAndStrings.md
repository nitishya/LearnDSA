𝗔𝗿𝗿𝗮𝘆𝘀 𝗮𝗻𝗱 𝗦𝘁𝗿𝗶𝗻𝗴𝘀:
1. Find the maximum sum subarray.
2. Find all substrings that are palindromes.
3. Implement the "two sum" problem.
4. Implement Kadane's algorithm for maximum subarray sum.
5. Find the missing number in an array of integers.
6. Merge two sorted arrays into one sorted array.
7. Check if a string is a palindrome.
8. Find the first non-repeating character in a string.
9. Write a program to remove duplicates from a sorted array.

---
1. Find the maximum sum subarray.
```
package arraysString;
import java.util.Arrays;
import java.util.OptionalInt;

public class MaximumSubArray {

	static int maxArraySum(int[] arr) {

		OptionalInt res = Arrays.stream(arr).reduce((m, c) -> {
			int newMaxSum = Math.max(c, m + c);
			return newMaxSum;
		});
		return res.orElse(0);
	}

	public static void main(String[] args) {
		System.out.println("printing output");
		int[] arr = { 2, 3, -8, 7, -1, 2, 3 };
		System.out.println(maxArraySum(arr));

	}
}

```


