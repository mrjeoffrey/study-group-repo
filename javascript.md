// What is the syntax to assign a variable?

// What is the syntax to create an array?

// What is the syntax to create an object?

// Name 3 if conditions

// Name 3 ways to define a function

// Name 5 ways to create loops

// What is the appropriate syntax to create if conditions?

// What is the appropriate synxtax to define a function?

// What is the appropriate syntax to create loops?

// What are 10 commonly used string methods?

// What are 10 commonly used array methods?

// How do you traverse the DOM without specificity?

// How do you traverse the DOM with specificity?

// Show me one way to use timeInterval method?

// How do you store data from variables into the local storage?

// How do you see stored data in the browser, for example CHROME?

// How do you get data from local storage to appear on the HTML Doc?

// What does preventDefault() do?

// What are some usecases to use preventDefault()?

// Why is console.log() important?
- - -
To add add one event listener with the same function to multiple elements
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
 
 - - -
 
//In javascript, to set a CSS class to newly created item:

//use "yourVariable".className = "css-class-name"

// remove() deletes each element

//while loops already exist within functions(will keep running until if condition breaks)

- - -
 
 How do you reverse a string in-line, given the elements of the string are in an array? ex: ["h", "e", "l", "l", "o"]
 
 <details>
  <summary>Solution</summary>
  
 
```
function reverseString(string) {
    string = string.reverse()
}
```
</details>

- - -
  
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
 <details>
  <summary>Solution 1 </summary>
  
  
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
  <summary>Solution 1 </summary>
  
 
```
var twoSum = function(nums, target) {
    var newList = [];
    for (var x = 0; x < nums.length; x++) {
    if (nums.includes(target - nums[x])) {
        newList = [nums.indexOf(target - nums[x]), nums.indexOf(nums[x])];
        }
    }
    return newList;
};
```
</details>
