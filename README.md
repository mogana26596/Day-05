# Day-05
1. Do the below program in anonymous function & IIFE function:
a. Print odd numbers in an array
Anonymous function:
var odd=function(num){
  for (let i=0;i<num.length;i++) 
  {
    if(num[i]%2!=0)
    {
      console.log(num[i]);
    }
  }
}
console.log(odd([1,2,3,4,5]));

IIFE function:
(function(num) {
  for (let i=0;i<num.length;i++) 
  {
    if(num[i]%2!=0)
    {
      console.log(num[i]);
    }
  }
})
([1,2,3,4,5]);

b. convert all the string to title caps in string array 
Anonymous function:
var   toTitleCase = function(str) {
  return str.toLowerCase().split(' ').map(function (word) {
    return (word.charAt(0).toUpperCase() + word.slice(1));
  }).join(' ');
}
console.log(toTitleCase("guvi geeks"));

IIFE function:
(function(str) {
        console.log (str.toLowerCase().split(' ').map(function (word) {
   console.log (word.charAt(0).toUpperCase() + word.slice(1));
  }).join(' '));
})
("guvi geeks");

c. Sum of all numbers in an array
Anonymous function:
var num = function (a,b,c) {
        return (a+b+c);
}
console.log(num (30,14,5));

IIFE function:
(function (a,b,c) {
console.log (a+b+c);
})
 (30,14,5);

d. Return prime number in array
Anonymous function:
var isPrime = function(n)
{
      if(n == 1 || n == 0) return false;
      for(var i = 2; i < n; i++)
      {    
        if(n % i == 0) return false;
      }
            return true;
}
var N = 10;
   for(var i = 1; i <= N; i++)
  {
        if(isPrime(i)) {
        console.log( i );
      }
}
 console.log(isPrime(2));

IIFE function:
(function isPrime (n)  {
{
      if(n == 1 || n == 0) return false;
      for(var i = 2; i < n; i++)
      {    
        if(n % i == 0) return false;
      }
            return true;
}
  for(var i = 1; i <= 10; i++)
  {
        if(isPrime(i)) {
        console.log( i );
      }
}
})
();

e. Return palindromes in an array 
Anonymous function:
var  palindromize = function (words) {
    var p = words.split("").reverse().join("");

    if(p === words){
        return(words);
    } else {
        return("0");
    }
}
console.log (palindromize (“viicc”, “cecarar”, “honda”));

IIFE function:
(function (words) {
    var p = words.split("").reverse().join("");

    if(p === words){
        return(words);
    } else {
        return("0");
    }
})
 (“viicc”, “cecarar”, “honda”);

f. Return median of two sorted arrays of same size 
Anonymous function:
var median = function (ar1, ar2, n){
    var i = 0; 
    var j = 0;
    var count;
    var m1 = -1, m2 = -1;
    for (count = 0; count <= n; count++)
    {
        if (i == n)
        {
            m1 = m2;
            m2 = ar2[0];
            break;
        }
         else if (j == n)
        {
            m1 = m2;
            m2 = ar1[0];
            break;
        }
        if (ar1[i] <= ar2[j])
        {
            m1 = m2;
            m2 = ar1[i];
            i++;
        }
        else
        {
            m1 = m2;
            m2 = ar2[j];
            j++;
        }
    }
      return (m1 + m2)/2;
}
Console.log (median ([1, 12, 15, 26, 38],[2, 13, 17, 30, 45], 3));

IIFE function:
(function (ar1, ar2, n){
    var i = 0; 
    var j = 0;
    var count;
    var m1 = -1, m2 = -1;
    for (count = 0; count <= n; count++)
    {
        if (i == n)
        {
            m1 = m2;
            m2 = ar2[0];
            break;
        }
         else if (j == n)
        {
            m1 = m2;
            m2 = ar1[0];
            break;
        }
        if (ar1[i] <= ar2[j])
        {
            m1 = m2;
            m2 = ar1[i];
            i++;
        }
        else
        {
            m1 = m2;
            m2 = ar2[j];
            j++;
        }
    }
      return (m1 + m2)/2;
})
([1, 12, 15, 26, 38],[2, 13, 17, 30, 45], 3);

g. Remove duplicates from an array
Anonymous function:
var duplicates = function (arr){
        let un = [];
           for(let i of arr) {
        if(un.indexOf(i) === -1) {
            un.push(i);
        }
    }
    console.log(un);
}
console.log(duplicates ([1, 2, 3, 2, 3]);

IIFE function:
(function (arr){
        let un = [];
           for(let i of arr) {
        if(un.indexOf(i) === -1) {
            un.push(i);
        }
    }
    console.log(un);
})
([1, 2, 3, 2, 3]);

h. Rotate an array by k times
Anonymous function:
var arrayRotate = function(arr, reverse) {
  if (reverse) arr.unshift(arr.pop());
  else arr.push(arr.shift());
  return arr;
}
console.log (arrayRotate([1, 2, 3, 4, 5]));

IIFE function:
(function(arr, reverse) {
  if (reverse) arr.unshift(arr.pop());
  else arr.push(arr.shift());
  console.log (arr);
})
([1, 2, 3, 4, 5]);


3. Do the below program in arrow function:
a. Print odd numbers in an array
var odd= (num) => {
  for (let i=0;i<num.length;i++) 
  {
    if(num[i]%2!=0)
    {
      console.log(num[i]);
    }
  }
}
console.log(odd([1,2,3,4,5]));

b. convert all the string to title caps in string array 
var   toTitleCase = (str) => {
  return str.toLowerCase().split(' ').map(function (word) {
    return (word.charAt(0).toUpperCase() + word.slice(1));
  }).join(' ');
}
console.log(toTitleCase("guvi geeks"));

c. Sum of all numbers in an array
var num = (a,b,c) => {
        return (a+b+c);
}
console.log(num (30,14,5));

d. Return prime number in array
var isPrime = (n) => {
      if(n == 1 || n == 0) return false;
      for(var i = 2; i < n; i++)
      {    
        if(n % i == 0) return false;
      }
            return true;
}
var N = 10;
 
  for(var i = 1; i <= N; i++)
  {
        if(isPrime(i)) {
        console.log( i );
      }
}
 console.log(isPrime(2));

e. Return palindromes in an array 
var  palindromize = (words) => {
    var p = words.split("").reverse().join("");

    if(p === words){
        return(words);
    } else {
        return("0");
    }
}
console.log (palindromize (“viicc”, “cecarar”, “honda”));
