---
title: "Day 2 - 30 days of javascript"

date: "2022-12-20"

tags: ["learning"]


links:
    # website: 'https://github.com/hadisinaee/avicenna'
    # alias: link_name_here
---

### Check if typeof '10' is exactly equal to 10. If not make it exactly equal.

```javascript
const string = '10';
const number = 10;
//using casting
let stringNumber = parseInt(string);
if (stringNumber == number) {
    console.log("equal")
}
```

### Check if parseFloat('9.8') is equal to 10 if not make it exactly equal with 10.

```javascript
let strNumber = '9.8';
let number = 10;
if (strNumber != number) {
    console.log("not equal");
}
let intNumber = parseInt(strNumber);
let intNumberTen = intNumber + 1;
if (intNumberTen == number) {
    console.log("equal");
}
```


### Check if 'on' is found in both python and jargon

```javascript
let string = "python";
let string2 = "jargon";
let searchWord = string.includes('on');
let searchWord2 = string2.includes('on');
if (searchWord && searchWord2 == true) {
    console.log("true");
}
```

###  Generate a random number between 50 and 100 inclusively.
```javascript
function getRndNumber(min, max) {
    let numberRnd = Math.floor(Math.random() * (max - min + 1)) + min;
    return numberRnd;
}
let getNumber = getRndNumber(50, 100);
console.log(getNumber);
```

### Access the 'JavaScript' string characters using a random number.
```javascript
let string = 'JavaScript'
let stringLength = string.length;
let getRndIndex = Math.floor(Math.random() * stringLength);
let toIndex = parseInt(getRndIndex);
let accessString = string.charAt(toIndex);
console.log(accessString);
```

### Use substr to slice out the phrase because because because from the following sentence:'You cannot end a sentence with because because because is a conjunction'
```javascript
let string = 'You cannot end a sentence with because because because is a conjunction'
let string2 = string.substr(31, 23);
let final = string.replace(string2, '');
console.log(final);
```

### 'Love is the best thing in th``is world. Some found their love and some are still looking for their love.' Count the number of word love in this sentence.

```javascript
let string = 'Love is the best thing in this world. Some found their love and some are still looking for their love.'
let count = (string.match(/love/ig) || []).length;
console.log(count);
```

### Use match() to count the number of all because in the following sentence :'You cannot end a sentence with because because because is a conjunction'

```javascript
let string = 'You cannot end a sentence with because because because is a conjunction';
let word = /because/gi
console.log(string.match(word));
```

### Clean the following text and find the most frequent word (hint, use replace and regular expressions).

``` javascript
const sentence = '%I $am@% a %tea@cher%, &and& I lo%#ve %te@a@ching%;. The@re $is no@th@ing; &as& mo@re rewarding as educa@ting &and& @emp%o@weri@ng peo@ple. ;I found tea@ching m%o@re interesting tha@n any ot#her %jo@bs. %Do@es thi%s mo@tiv#ate yo@u to be a tea@cher!? %Th#is 30#Days&OfJavaScript &is al@so $the $resu@lt of &love& of tea&ching'
let pattern = /[!@#$%^&*?;]/g;
let result = sentence.replace(pattern, '')
var wordCounts = {};
var words = result.split(/\b/);
console.log(words);
for (var i = 0; i < words.length; i++) {
    // loop through the words and increment a counter for each one;
    wordCounts[words[i]] = (wordCounts[words[i]] || 0) + 1;
}
console.log(wordCounts);
// console.log(sentence.replace(pattern, ''));
```
### Calculate the total annual income of the person by extracting the numbers from the following text. 'He earns 5000 euro from salary per month, 10000 euro annual bonus, 15000 euro online courses per month.'
```javascript
let string = 'He earns 5000 euro from salary per month, 10000 euro annual bonus, 15000 euro online courses per month.';

let pattern = /\d+/g

let result = string.match(pattern);

let calIncome = (parseInt(result[0]) * 12) + parseInt(result[1]) + (parseInt(result[2]) * 12);

  

console.log(calIncome);
```