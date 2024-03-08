## Meta 정보
- [type]: editor
- [id]: 5330
- [duration]: 300
- [language]: javascript
- [difficulty]: 1

## Question
```html
<p>
  In a dice game, you're provided with an array named <code>results</code> that records the outcomes of several rounds. Each object in the array represents a round's scores for "me" and the "opponent". 
  <br>The winner is the one with the higher total points. 
  <br>Print 'me' if you have more points, or 'opponent' if the opponent has more.
</p>
```

## Instruction
### language
- KO
```html
<ul>
    <li>
        Iterate over the <code>results</code>.
    </li>
    <li>
        Accumulate the scores from all rounds by adding each round's score for "me" and "opponent" to the respective <code>myPoints</code> and <code>opponentPoints</code> variables.
    </li>
</ul>
```
- EN

## Editor
### language
- KO
```javascript
const results = [
    {me: 4, opponent: 6}, {me: 1, opponent: 2}, {me: 4, opponent: 2},
    {me: 2, opponent: 2}, {me: 3, opponent: 6}, {me: 1, opponent: 2},
    {me: 3, opponent: 4}, {me: 5, opponent: 3}];

let myPoints = 0;
let opponentPoints = 0;

// Type code from here


//////////////////////////////////////////////////////////
// Please do not delete the code below for evaluation of your code
console.log(myPoints > opponentPoints ? "me" : "opponent");
```
- EN

## Correct Answer
```javascript
const results = [
    {me: 4, opponent: 6}, {me: 1, opponent: 2}, {me: 4, opponent: 2},
    {me: 2, opponent: 2}, {me: 3, opponent: 6}, {me: 1, opponent: 2},
    {me: 3, opponent: 4}, {me: 5, opponent: 3}];

let myPoints = 0;
let opponentPoints = 0;

// Type code from here
for(let result of results) {
    myPoints += result.me;
    opponentPoints += result.opponent;
}

//////////////////////////////////////////////////////////
// Please do not delete the code below for evaluation of your code
console.log(myPoints > opponentPoints ? "me" : "opponent");
```

## Output
opponent