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
    return arrayNumbers.reduce( (a,b) => { return a + b;} ) % 2 == 0 ? "Even" : "Odd";
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

### Is Palindrome, week 2:
```javascript
function isPalindrome(line){
    let word = String(line);
    let auxWord = "";
    for (let i = word.length-1; i >= 0; i-- ){
        auxWord += word[i];
    }
    return word === auxWord ? true : false;
}
```

### Well of ideas, week 2:
```javascript
function isPalindrome(line){
    let word = String(line);
    let auxWord = "";
    for (let i = word.length-1; i >= 0; i-- ){
        auxWord += word[i];
    }
    return word === auxWord ? true : false;
}
```

### React manage events, week 2:
```react
import React from 'react';

export class Counter extends React.Component {
  constructor(props) {
    super();
    this.state = {counter: 0}
  }
  
  incrementCounter = () => {
    this.setState([{counter: this.state.counter++}])
  }
  
  decrementCounter = () => {
    this.setState([{counter: this.state.counter--}])
  }
  
  // Your event handlers 
  render() {
    return (
      <div>
        <h1>{this.state.counter}</h1>
          <button id="increment" type="button" onClick={this.incrementCounter}>
            Decrement
          </button>
          <button id="decrement" type="button" onClick={this.decrementCounter}>
            Increment
          </button>
          <a id="counter">{this.state.counter}</a>
      </div>
    )
  }
}
```
