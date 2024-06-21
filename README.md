# array-to-string
# 1. Joining array elements into a string

// Sample array
let myColor = ["Red", "Green", "White", "Black"];

// Expected Output: "Red,Green,White,Black" "Red,Green,White,Black" "Red+Green+White+Black"
let joinedByComma = myColor.join(",");
let joinedBySpace = myColor.join(" ");
let joinedByPlus = myColor.join("+");

console.log(joinedByComma);  // Output: "Red,Green,White,Black"
console.log(joinedBySpace);  // Output: "Red Green White Black"
console.log(joinedByPlus);   // Output: "Red+Green+White+Black"

# 2. Finding the most frequent element in an array

// Sample array
let arr1 = [3, 'a', 'a', 'a', 2, 3, 'a', 3, 'a', 2, 4, 9, 3];

function mostFrequent(arr) {
    let frequency = {};
    let maxCount = 0;
    let mostFrequentElement = null;

    for (let element of arr) {
        frequency[element] = (frequency[element] || 0) + 1;
        if (frequency[element] > maxCount) {
            maxCount = frequency[element];
            mostFrequentElement = element;
        }
    }

    return `${mostFrequentElement} (${maxCount} times)`;
}

console.log(mostFrequent(arr1));  // Output: "a (5 times)"

# 3. Truncating a string

function truncateString(str, num) {
    return str.slice(0, num);
}

console.log(truncateString("Robin Singh", 4));  // Output: "Robi"

# 4. Capitalizing the first letter of each word in a string

function capitalizeWords(str) {
    return str.split(' ').map(word => word.charAt(0).toUpperCase() + word.slice(1)).join(' ');
}

console.log(capitalizeWords('js string exercises'));  // Output: "Js String Exercises"

# 5. Filtering an array to only include elements between two values

function arrBetween(num1, num2, arr) {
    return arr.filter(item => item >= num1 && item <= num2);
}

console.log(arrBetween(3, 8, [1, 5, 95, 0, 4, 7]));  // Output: [5, 4, 7]
console.log(arrBetween(1, 10, [1, 10, 25, 8, 11, 6]));  // Output: [1, 10, 8, 6]
console.log(arrBetween(7, 32, [1, 2, 3, 78]));  // Output: []

# 6. Finding the index of a specific element in an array

function findIndex(arr, element) {
    return arr.indexOf(element);
}

console.log(findIndex(["hi", "edabit", "fgh", "abc"], "fgh"));  // Output: 2
console.log(findIndex(["Red", "blue", "Blue", "Green"], "blue"));  // Output: 1
console.log(findIndex(["a", "g", "y", "d"], "d"));  // Output: 3
console.log(findIndex(["Pineapple", "Orange", "Grape", "Apple"], "Pineapple"));  // Output: 0
