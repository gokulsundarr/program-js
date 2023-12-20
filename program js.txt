/*Print odd numbers in an array*/

const numbers = [8, 19, 5, 6, 14, 9, 13];
const odds = [];
numbers.forEach((num) => {
  if (num % 2 === 1) {
    odds.push(num);
  }
});
console.log(odds); 

/*Convert all the strings to title caps in a string array*/


function sentenceCase(str) {
    if ((str === null) || (str === ''))
        return false;
    else
        str = str.toString();
 
    return str.replace(/\w\S*/g,
        function (txt) {
            return txt.charAt(0).toUpperCase() +
                txt.substr(1).toLowerCase();
        });
}
 
console.log(sentenceCase('welcome to the program'));

/*Sum of all numbers in an array */

let arr = [4, 8, 7, 13, 12]
 
let sum = 0;
 

for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
}
 
console.log("Sum is " + sum) ;

/*Return all the prime numbers in an array*/

var a = [5, 9, 63, 29, 35, 6, 55, 23]
var prime = [];

function isPrime(item) {
    var identifier = item / 2;
      for (var j = 2; j <= identifier; j++) {
       if ((item % j) == 0) { 
        return false;
       } 
     }
     return true;
}
for (var index = 0; index < a.length; index++) {
  if (isPrime(a[index])) {
      prime.push(a[index])
  }
}

console.log(prime);

/*Return all the palindromes in an array*/

function isPalindrome(s)
{
    
    let a = s;
    s = s.split('').reverse().join('');
   
    return s == a;
}
 
function PalindromicStrings(arr,N)
{
    let ans = [];   
    for (let i = 0; i < N; i++) {
 
        if (isPalindrome(arr[i])) {
 
            ans.push(arr[i]);
        }
    }
    return ans;
}
 
let arr = [ "abc", "car", "ada", "racecar", "cool" ];
let N = arr.length;
 
let s = PalindromicStrings(arr, N);
if(s.length == 0)
    console.log("-1");
for(let st of s)
    console.log(st," ");
 
/*Remove duplicates from an array*/

let arr= ["apple", "mango", "apple",
          "orange", "mango", "mango"];
 
function removeDuplicates(arr) {
    return arr.filter((item,
        index) => arr.indexOf(item) === index);
}
console.log(removeDuplicates(arr));

/*Rotate an array by k times*/


function RightRotate(a, n, k) 
{ 
  
    k = k % n; 
  
    for (let i = 0; i < n; i++) { 
        if (i < k) { 
  
           
            console.log(a[n + i - k] + " "); 
        } 
        else { 
  
           
            console.log((a[i - k]) + " "); 
        } 
    } 
    console.log("<br>"); 
} 
  

let Array = [1, 2, 3, 4, 5]; 
let N = Array.length; 
let K = 2; 
  
RightRotate(Array, N, K); 
 