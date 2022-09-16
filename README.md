# Challenges

## Ensure question, week 1:
```javascript
function wordWithQuestionMark(word){
    return word.endsWith('?') ? word : word += "?";
}
```
## Odd or even, week 1:
```javascript
function oddOrEven(arrayNumbers){
    if (arrayNumbers.length == 0) return "Even";
    return Number.isInteger(arrayNumbers.reduce( (a,b) => { return a + b;} ) / 2 ) ? "Even" : "Odd";
}
```

## Reversed words, week 1:
```javascript
function reverseWords(originalWord){
    return originalWord.split(" ").reverse().toString().replaceAll(",", " ");
}
```

## Smallest integer in array, week 1:
```javascript
function smallestIntegerInArray(arrayNumbers){
    return Math.min.apply(Math, arrayNumbers);
}
```
