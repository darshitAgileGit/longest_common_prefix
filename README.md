## Finding the Longest Common Prefix

One of the classic problems in computer science and coding interviews is finding the Longest Common Prefix among an array of strings. This problem involves writing a function that takes an array of strings and returns the longest prefix shared by all the strings. If there is no common prefix, the function should return an empty string.

### Problem statement
Given an array of strings, determine the longest common prefix string. If no common prefix exists, return an empty string ("").

##### Examples
```$xslt
const arrayOne = ['car', 'care', 'cash', 'cake', 'camera']
// Output: "ca"

const arrayTwo = ['pen', 'flash', 'place', 'kick', 'ball'];
// Output: ""
```

### Proceed towards solution

> The solution can be proceeded by the following steps.

1. Use the first string in the array for the reference for comparison.
2. Compare each character of the first string with the corresponding character of all other strings in the array.
3. If a mismatch is found at any position, return the prefix built so far. If all character match, continue building the prefix.

### Solution
- Let's breakdown the solution step by step.

1. Begin with an empty prefix string.
2. If the input array is empty, return the empty prefix.
3. For each character in the first string, check if it matches the corresponding character in all other strings.
4. If a mismatch is found, return the prefix. Otherwise, add the character to the prefix.
5. After extracting all characters, return the longest common prefix.

### Let's code
```$xslt
function longestCommonPrefix(array) {

    let prefix = '';

    // Return empty prefix if array is empty
    if (array.length === 0) {
        return prefix;
    }

    // Use the first element for reference
    const firstElement = array[0];

    // Iterate over each character of the first element
    for (let i = 0; i < firstElement.length; i++) {
        const char = firstElement[i]

        // Compare the character with the corresponding character in all other strings
        for (let j = 1; j < array.length; j++) {
            if (array[j][i] !== char) {
                return prefix
            }
        }
        // If the character matches in all strings, add it to the prefix
        prefix = prefix + char;
    }
    // Return the final prefix
    return prefix
}
``` 

### Explanation
- Begin with an empty string as the prefix.
- If the input array is empty, return the empty prefix straight away.
- Use the first string as the reference for comparison.
- For each character in the first string, check if it matches the corresponding character in all other strings.
- If a character mismatch is found at any position, return the prefix built so far. Otherwise, add the character to the prefix.
- Return the longest common prefix after processing all characters of the first string.

### Learning
> Here I will tell you what I have learned from this problem.

- As you can see in our solution, we utilized nested loops to perform comparisons. Nested loops prove to be effective in comparing elements across multiple levels of data structures.
- I learned that how to use nested loops to compare characters at definite positions across multiple strings. The outer loop iterates over each character of the reference string, while the inner loop iterates over each element of the main array.

### Stay Tuned!

Stay tuned for more coding challenges and insightful solutions! Keep practicing and enhancing your problem-solving skills. Happy coding!
