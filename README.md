## Researching prompt 1 - turning strings to URLs
* how many spaces? 


### example
* // Given n, return the nth number (number at the position of n) of the Fibonacci Sequence where n >= 1

* // n = 7
* // 8
* // 0, 1, 1, 2, 3, 5, 8, ...

* // Clarifying Questions
* // What is the Fib?
* // MAy I use JS/C#?
* // What about my inputs? Always positive? Account for strings?
* // Error handling?
* // Can I use built-in methods?

* // Pseudocoding
* // Accept N, a positive integer (N >= 1) // DONE
* // Something like a loop to do this:
* // Count up to the Nth positiong using addition to get to said Nth number. // DONE
* // Add the previous two numbers together to get the next. // DONE
* // Figure out a way to keep track of these numbers to add them upp as I go. 
* // Put them in an array? (.push())
* // Figure out how to get the value at N
* // Return said value. 

### my prompt

Question #3: Compressing Strings
Write an algorithm that takes a string with repeated characters and compresses them, using a number to show how many times the repeated character has been compressed. For instance, aaa would be written as 3a. Solve the problem with and without recursion.

Example
Input: "aaabccdddda"

Output: "3ab2c4da"

function compress(string) {
  let outputString = "";
  let currentLetter = string[0];
  let count = 1;
  for (let i = 1; i < string.length; i++) {
    if (string[i] === currentLetter) {
        count++;
    } else if (count !== 1) {
        outputString += count + currentLetter;
      currentLetter = string[i];
      count = 1;
    } else {
        outputString += currentLetter;
      currentLetter = string[i];
    }
  }
  if (count === 1) {
      outputString += currentLetter;
  } else {
      outputString += count + currentLetter;
  }
  console.log(outputString);
}

compress("aaabccdddda");