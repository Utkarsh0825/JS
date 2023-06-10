# JS
1. If the given input is an array of numbers, return the sum of all the positives ones. If the array is empty or there aren't any positive numbers, return 0.
const input = [1, -4, 12, 0, -3, 29, -150];

Answer
const input = [1, -4, 12, 0, -3, 29, -150];

const sumPositiveNumbers = (arr) => {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] > 0) {
            sum += arr[i];
        }
    }
    return sum;
}

console.log(sumPositiveNumbers(input));

//Output
42

2. Square the value of every element in the array. Presume that you will only get numbers in the input array.
const input = [1, 2, 3, 4, 5];

Answer
const input = [1, 2, 3, 4, 5];

const squareArray = (arr) => {
    let result = [];
    for (let i = 0; i < arr.length; i++) {
        result.push(arr[i] * arr[i]);
    }
    return result;
}

console.log(squareArray(input)); 
//Output
[ 1, 4, 9, 16, 25 ]
 



4.Find the difference in age between the oldest and youngest family members, and return their respective ages and the age difference.


const input = [
 {
   name: "John",
   age: 13,
 },
 {
   name: "Mark",
   age: 56,
 },
 {
   name: "Rachel",
   age: 45,
 },
 {
   name: "Nate",
   age: 67,
 },
 {
   name: "Jennifer",
   age: 65,
 },
];



Answer
const ageDifference = (arr) => {
    let minAge = arr[0].age;
    let maxAge = arr[0].age;
    for (let i = 1; i < arr.length; i++) {
        if (arr[i].age < minAge) {
            minAge = arr[i].age;
        }
        if (arr[i].age > maxAge) {
            maxAge = arr[i].age;
        }
    }
    return {oldest: maxAge, youngest: minAge, difference: maxAge - minAge};
}

console.log(ageDifference(input));
 // Output:
 { oldest: 67, youngest: 13, difference: 54 }




5. If the given input is a number, you should return the factorial of that number. The factorial of a natural number n is the product of the positive integers less than or equal to n. So, 2! = 2, 3! = 6, 4! = 24 and so on.


Answer
const factorial = (n) => {
    let result = 1;
    for (let i = 1; i <= n; i++) {
        result *= i;
    }
    return result;
}

console.log(factorial(2)); // Output: 2
console.log(factorial(3)); // Output: 6
console.log(factorial(4)); // Output: 24
