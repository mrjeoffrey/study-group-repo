What is the syntax to assign a variable?

What is the syntax to create an array?

<details>
  <summary>Solution</summary>
```
const array = [];
```
</details>

What is the syntax to create an object?

Name 3 if conditions

Name 3 ways to define a function

<details>
  
  <summary>Solution</summary>
  
  ```
  const, let, or var
  
  ```
  
</details>

Name 5 ways to create loops

What is the appropriate syntax to create if conditions?

What is the appropriate synxtax to define a function?

```
function functionName() {}
//OR
var functionName = function() {}
```

What is the appropriate syntax to create loops?

What are 10 commonly used string methods?

What are 10 commonly used array methods?

How do you traverse the DOM without specificity?

How do you traverse the DOM with specificity?

Show me one way to use timeInterval method?

How do you store data from variables into the local storage?

```
localStorage.setItem("storedItem", value);
//To retrieve:
localStorage.getItem("storedItem");
//Assign to a variable 'stored':
const stored = localStorage.getItem("storedItem");
```


How do you see stored data in the browser, for example CHROME?

How do you get data from local storage to appear on the HTML Doc?

What does preventDefault() do?

What are some usecases to use preventDefault()?

Why is console.log() important?

To add add one event listener with the same function to multiple elements:

<details>
  <summary>Solution</summary>
    
```
document.addEventListener("click"), function(event) {
    if (event.target.matches("element-class-name")) {
        *do something*
    }
 }
 ```
    
 </details>
 
 
In javascript, to set a CSS class to newly created item:

use "yourVariable".className = "css-class-name"

remove() deletes each element

while loops already exist within functions(will keep running until if condition breaks)

- - -

# Leetcode Questions and Solutions(Feel free to enter your own solutions or ones you've found!)
 
 How do you reverse a string in-line, given the elements of the string are in an array? ex: ["h", "e", "l", "l", "o"]
 
 <details>
  <summary>Solution 1(Marcus) Time Complexity: O(N)</summary>
  
  ```
  function reverseString(string) {
    //Creates an empty string for temporary use.
    var tempString = "";
    //Converts the original array to a string value 's'.
    s = string.join("");
    //For each element in the string 's', adds the last element of string 's'
    //to the first available position in 'tempString'.
    //We start with 'y = s.length' and want to reduce 'y' for the purpose of
    //iterating through each element, as the length is ever decreasing.
    //If you tried to start with 'y = 0' and increase 'y' each iteration,
    //You would not concat a certain amount of elements in the string, as the
    //value of 'y' and 's.length' approach.
    for (let y = s.length; y > 0; y--) { 
        tempString = tempString.concat(s.charAt(y - 1));
        //Removes the last item from the string 's' to not repeat letters.
        s = s.slice(0, y - 1);
    }
    //Reassign the 's' string to tempString.
    s = tempString;
    //Reassign the 'string' to 's.split("")', which creates a new array, separating
    //each element.
    string = s.split("");
}
```
</details>

 <details>
   
  <summary>Solution 2(Google) Time Complexity: O(1)</summary>
  
 
```
function reverseString(string) {
    string = string.reverse()
}
```
</details>

- - -
  
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
 <details>
  <summary>Solution 1(Google) Time Complexity: O(N^2)</summary>
  
  
```
var twoSum = function(nums, target) {
    for (var x = 0; x < nums.length; x ++) {
        for (var y = x+1; y < nums.length; y++) {
        if(nums[x] + nums[y] == target) {
            var sum = [x,y];
            return sum;
        }
      }
   }
};
```
</details>
  
<details>
  <summary>Solution 2: (Marcus) Time Complexity: O(N)</summary>
  
  ```
//Two sum function.
var twoSum = function(nums, target) {
    //Iterates over the length of the array.
    for (var x = 0; x < nums.length; x++) {
        //Assign a variable 'match' to the difference between the target 
        //and the 'x' index in the array.
        var match = target - nums[x];
        //Assign a variable 'index' to the 'match' variable's index value,
        //after the first 'x' index.
        //This is done to avoid assigning the index to the 'x' index
        //in the case that the target is a double of the 'x' index.
        //The value of 'index' is assigned '-1' if the 'match' value 
        //does not exist within the array. 
        var index = nums.indexOf(match, x+1);
        //Checks for an existing 'match' via 'index' check.
        if (index != -1) {
            //If a 'match' is found('index' does not equal '-1'):
            //Assign an array 'newList' to the values of the index
            // of 'x' and 'index'.
            var newList = [nums.indexOf(nums[x]), index];
            //Returns the newList containing the correct indices.
            return newList;
        }
        //The 'x' index increases if the 'x' index value itself is not
        //one of the available matching values.
    }
};

      
//Example:
numbers = [6,-18,7,9];
target = -9;
twoSum(numbers, target); //Expected output: [1,3]     
```
</details>
