# Vue Component Notes 
### October 12, 2017

* this flips the thingy
```
this.flip = !this.flip; // reverses the card's class
```



# the $emit statement
## this is one way components talk to each other

- this statement "emits" an event or puts it out into the atmostphere for event listeners to hear
	- creates a custom event
- it is coupled with a "on" statement that will listen for the particular event

```
this.$emit('cardFlipped', panelID); 
```
- create custom event and $emit it 


```
v-on:cardFlipped="alertFlip" /></card>
```
- listen for custom event with an "on" statement referencing the name of your custom event


# props


- the child function (cards) expects definitions for it's values from the parent component 
- props is where the child lists it's expectations
- in our card game, the card-child function expects the 'panelID' variable from the board-parent function
in child component...

```
props : [ 'panelID' ],
```


in parent (Board)...

```
<card panelID="A" 
```


# upstream flow of information
## (child)-->(parent)-->(App.vue)
- the comonents need to be explicitely connected to one another in a particular order so that the child function can reach the parent function, and the parent function can reach the app.vue

in parent component...
```
import Card from './Card.vue' 
```
- this connects to child component

in App.vue...
```
import Board from './components/Board.vue'
```


the child function (cards) expects definitions for it's values from the parent component 
within board-
