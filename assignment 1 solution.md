---
---

# 📘 JavaScript Exercises: Loops (`for`, `for...of`, `for...in`)

---

## 🔹 Level 1: Basics (`for` loop)

### 1. Print Elements

Print all elements of an array using a `for` loop.

```js```
let arr = [5, 10, 15];

```

```solution```
let arr = [5, 10, 15];

for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]);
};
```



---

### 2. Sum of Numbers

Find the sum of all elements in an array.

``` solution
let arr = [5, 10, 15];
let sum = 0;
for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
};

```

console.log(sum);
---

### 3. Find Minimum Value

Find the smallest number in an array.

```solution 
let arr = [5, 10, 15];
let min = arr[0];
for (let i = 0; i < arr.length; i++) {
        if (arr[i] < min) {
            min = arr[i];
        }
};

console.log(min);
---
```

### 4. Count Odd Numbers

Count how many odd numbers exist in an array?

```solution
let arr = [2, 11, 18];
let odd = arr[0];
for (let i = 0; i < arr.length; i++) {
        if (arr[i] % 2 !== 0) {
            odd = arr[i];
        }
};

console.log(odd);

---
```

### 5. Reverse Array (Manual)

Create a new reversed array using a `for` loop.
```solution```

let arr = [5, 10, 15];
let revArr = [];
for (let i = arr.length - 1; i >= 0; i--) {
       revArr.push(arr[i]);

};

console.log(revArr);

```
```
## 🔹 Level 2: `for...of` (Cleaner Array Iteration)

### 6. Print Using `for...of`

Print all values of an array using `for...of`.

```solution``` 
let arr = [5, 10, 15];
for (let element of arr)
{
    console.log(element)
}

```
---
```

### 7. Multiply All Values

Multiply each element by 2 and store in a new array.

```solution```
let arr = [5, 10, 15];
let multarr = [];
for (let element of arr)
{
    multarr.push(element * 2);
}

console.log(multarr);

```
---
```

### 8. Find String Lengths

Given an array of strings, create a new array with their lengths.

```javaScript```
["apple", "banana", "kiwi"];
```

```solution```
let fruits = ["apple", "banana", "kiwi"];
let lengthFruits = [];

for (let fruit of fruits)
{
    lengthFruits.push(fruit.length);
}

console.log(lengthFruits)

```

---

### 9. Count Vowels in Array

Count total vowels across all strings in an array.

---
```solution```

let fruits = ["apple", "banana", "kiwi"];
let countVowel = 0;

for (let name of fruits) {
    for (let vowel of name) {
        if (vowel === "a"|| vowel === "e" ||  vowel === "i" || vowel === "o" || vowel === "u") {
            countVowel = countVowel + 1;

        }
    }
}

console.log("Total Vowels: ", countVowel);

```

### 10. Find First Negative Number

Find the first negative number in an array using `for...of`.

```solution```
let numbers = [32, 44, -1, 0, -24];
let negNum = 0;

for (let number of numbers) {
    if (number <= -1)
    {
        console.log(number);
        break;  
    }
}

```
---

## 🔹 Level 3: `for...in` (Objects)

### 11. Print Object Keys

Print all keys of an object using `for...in`.

```js```
let obj = { a: 1, b: 2, c: 3 };
```
```solution```

let obj = { a: 1, b: 2, c: 3 };

for (let key in obj)
{
    console.log(key);
}

```
---

### 12. Print Values

Print all values from an object.

```solution```
let obj = { a: 1, b: 2, c: 3 };

for (let key in obj)
{
    console.log(obj[key]);
}

---
```
### 13. Count Properties

Count how many properties exist in an object.

```solution```
let obj = { a: 1, b: 2, c: 3 };
let count = null;

for (let key in obj)
{
    count++;
}

console.log(count)
---
```
### 14. Sum Object Values

Find the total of all numeric values in an object.
```solution```

let obj = { a: 1, b: 2, c: 3 };
let count = null;

for (let key in obj)
{
    count = count + obj[key];
}

console.log(count)

```
---

### 15. Find Key with Highest Value

Find which key has the highest value.

```solution```
let obj = { a: 1, b: 2, c: 3 };
let maxValue = null;
let maxKey = null;

for (let key in obj)
{
    if (obj[key] > maxValue)
    {
        maxValue = obj[key]
        maxKey = key;

    }
};

console.log(maxKey);

```

---

## 🔹 Level 4: Mixed Practice (Arrays + Objects)

### 16. Filter Adults

Using `for...of`, return users with age ≥ 18.

```js
let users = [
  { name: "Ali", age: 17 },
  { name: "Sara", age: 21 },
];
```
```solution```
let users = [
  { name: "Ali", age: 17 },
  { name: "Sara", age: 21 },
];

let adults = [];

for (let profile of users)
{
    if (profile.age > 18 )
        {
            adults.push(profile);
        }
}

console.log(adults);
```end```
---

### 17. Total Marks per Student

Calculate total marks for each student.

```js
let students = [
  { name: "A", marks: [80, 70, 60] },
  { name: "B", marks: [90, 85, 88] },
];
```
```solution```
let students = [
  { name: "A", marks: [80, 70, 60] },
  { name: "B", marks: [90, 85, 88] },
];

for (let student of students) 
  {
    let total = 0;
    for (let mark of student.marks) 
    {
        total += mark;
    }
    student.totalMarks = total;
    console.log(`${student.name}'s Total Marks: ${student.totalMarks}`);
}
console.log(students);
```end```
---

### 18. Count Word Frequency

Count how many times each word appears.

```js
["apple", "banana", "apple", "orange"];
```

👉 Output:

```js
{ apple: 2, banana: 1, orange: 1 }
```
```solution```
let fruits = ["apple", "banana", "apple", "orange"];
let totalFruits = {};
for (let fruit of fruits)
{
  totalFruits[fruit] = (totalFruits[fruit] || 0) + 1;
}
console.log(totalFruits);


---

### 19. Nested Object Loop

Print all values inside nested objects.

```js
let data = {
  user1: { age: 20 },
  user2: { age: 25 },
};
```
```solution```
let data = {
  user1: { age: 20 },
  user2: { age: 25 },
};


for (let user in data)
{
  console.log(`${user}: ${data[user].age}`);
}

---

### 20. Group by Property

Group items based on a property.

```js
let products = [
  { name: "Shirt", category: "Clothing" },
  { name: "Pants", category: "Clothing" },
  { name: "Phone", category: "Electronics" },
];
```

👉 Expected:

```js
{
  Clothing: ["Shirt", "Pants"],
  Electronics: ["Phone"]
}
```

```solution```
let products = [
  { name: "Shirt", category: "Clothing" },
  { name: "Pants", category: "Clothing" },
  { name: "Phone", category: "Electronics" },
];


let groupedProducts = {};
for (let product of products) {
  let category = product.category;
  if (!groupedProducts[category]) {
    groupedProducts[category] = [];
  }
  groupedProducts[category].push(product.name);
}
console.log(groupedProducts );

---
