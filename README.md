# 10.7-Maps-and-Sets-Exercise
# ****Maps and Sets Exercise****

## **Quick Question #1**

What does the following code return?

```jsx
new Set([1,1,2,2,3,4])

//Set(4) {1, 2, 3, 4}
```

## **Quick Question #2**

What does the following code return?

```jsx
[...new Set("referee")].join("")

//ref
```

## **Quick Questions #3**

What does the Map ***m*** look like after running the following code?

```jsx
let m = new Map();
m.set([1,2,3], true);
m.set([1,2,3], false);

//0: {Array(3) => true}
//1: {Array(3) => false}
```

## **hasDuplicate**

Write a function called hasDuplicate which accepts an array and returns true or false if that array contains a duplicate

```jsx
hasDuplicate([1,3,2,1]) // true
hasDuplicate([1,5,-1,4]) // false

const hasDuplicate = arr => {
    let aSet = new Set();
    arr.forEach(val => aSet.add(val));
    arr.length !== aSet.size ? true : false
}
```

## **vowelCount**

Write a function called vowelCount which accepts a string and returns a map where the keys are numbers and the values are the count of the vowels in the string.

```jsx
vowelCount('awesome') // Map { 'a' => 1, 'e' => 2, 'o' => 1 }
vowelCount('Colt') // Map { 'o' => 1 }

const vowelCount = str => {
    const vowels = ['a', 'e', 'i', 'o', 'u'];
    const myMap = new Map();
    const strLowerCase = str.toLowerCase();

    for (let char of strLowerCase){
        if (vowels.includes(char)){
            if(myMap.has(char)){
                myMap.set(char, myMap.get(char) + 1);
            } else {
                myMap.set(char, 1);
            }
        }
    }
return myMap;
}
```
