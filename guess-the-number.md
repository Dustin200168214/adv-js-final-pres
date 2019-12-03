[Go back to README?](./README.md)
# Guess The Number

Introducing Guess the Number game with Svelte's syntax
  * key differences with vanilla js and Vue.js
  * .svelte extension and html document
  * script tag positioning
  * binding values and running functions
  
This app lets the user input a `number` and then checks if the number is equal, higher or lower than the `answer`, outputting a `message` that guides the user towards the solution. This game is based off of [this vue example](https://codepen.io/Ykciricky/pen/QWWqPdM) that we did in class.

```html
<h1>{message}</h1>
<input type="text" bind:value={number}>
<button on:click={check}>Check</button>
<script>
	let message = 'Guess a number!'
	let number
	let answer = 75
	// Check if the guessed number is correct
	function check() {
		if(number == answer){
			message = "Correct"
		} else if(number < answer ) {
			message = "Higher"
		} else if (number > answer) {
			message = "Lower"
		} else {
			message = "Guess a number!"
		}
	}
</script>
```

Link to REPL: 

https://svelte.dev/repl/9866f3a1ad924d7aaf3ae3c4e4ada8f0?version=3.16.0