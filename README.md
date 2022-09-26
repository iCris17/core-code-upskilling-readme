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
```javascript
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

### React santa wish list, week 2:
```javascript
const React = require("react");

class WishlistForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      name: "",
      wish: "",
      priority: 1 
    }
    
    this.updateName = this.updateName.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
    this.updateWish = this.updateWish.bind(this);
    this.updatePriority = this.updatePriority.bind(this);
  }
  
  updateName(event){
    this.setState({name: event.target.value})
  }
  
  updateWish(event){
    this.setState({wish: event.target.value})
  }
  
  updatePriority(event){
    this.setState({priority: event.target.value})
  }
  
  handleSubmit(event){
    this.props.send(this.state);
    event.preventDefault();
  }
  
  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <input id="name" type="text" value={this.state.name} onChange={this.updateName} /> 
        <textarea id="wish" value={this.state.wish} onChange={this.updateWish}></textarea>
        <select id="priority" value={this.state.priority} onChange={this.updatePriority}>
          <option selected value="1">1</option>
          <option value="2">2</option>
          <option value="3">3</option>
          <option value="4">4</option>      
          <option value="5">5</option>
        </select>
      </form>
    );
  }
};
```

### Easter egg list in react js, week 2:
```javascript
import React from 'react';

export const EggList = (props) => {
  const eggs = props.eggs;
  return (
    <ul>
      {eggs.map((item, index) => {
        return(
          <EasterEgg key={index} name={item}/>  
        )
      })}
    </ul>  
  )
};

export const EasterEgg = (props) => {
  return (
    <li>{props.name}</li>
  )
};
```
