this is from a message I posted in the slack channel "need help"

caseydemo [9:42 PM] 
in our tic-tac-toe app I am having trouble with messaging the main vue instance. What I think happens is: 
1. on:click calls the function callSquare, 
2. callSquare $emits the custom event 'new', 
3. the custom event 'new' is heard by the v-on:new in Index.html and calls "newClick" --- also v-bind:grid-location='TL' shooouuuuuld be assigning the grid location's value to 'TL' (top left square)
4. newClick(gridLocation) is called and heres the problem - when I console.log the gridLocation I keep getting undefined. 
*another thing I have noticed is that gridLocation is showing up in props with the correct value, but not the main Vue instance.


solution

the problem was that I wasn't getting good information back to the main Vue app file. to pass in the information I had to do use a "prop" - which as I understand it is basically a variable that I pass to a child component. In this case the parent is the HTML tag and the "child" is the actual vue instance. heres what I mean:

index.html:
```
<div is="space" grid-location="1" v-bind:symbol="markers[turn%2]" v-on:new="newClick"...
```

in index.html I set a static variable or "prop" to act as an identifier for that particular space on the gameboard. This got passed back to the vue app this was...

vue app:
```
var app = new Vue({

  el: '#app',
  data: {
  	markers: ['X', 'O'],
  	turn: 0,
  	gridLocation: ''
  	

  },
  methods: {
  	newClick: function( test ){
  		
  		this.gridLocation=test;
  		
  		this.turn++;
  		this.checkForWin();
  		this.checkForDraw();
  	}, 
```

so I made an empty data entity for gridLocation (what I established in the index.html page), and down in methods when newClick is called it receives a value - which I am calling test. This test value is the value sent from gridLocation - so now gridLocation is available to be used within the main vue app. 