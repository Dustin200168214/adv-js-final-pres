[Go back to README?](./README.md)
# If, else, each blocks
These blocks give us a way to conditionally render markup, which is not possibible in HTML.
## Guess the number IF blocks and ELSE blocks
An easier way to code the guess the number game presented by Ric through the use of Svelte's If and Else statements.
- Reducing the amount of code used for the game
- Svelte syntax for If and Else stetements
- Reactive

```html
<script>
	let number 
	let answer = 75
</script>
<h1>
{#if number == answer }
	Winner
{:else if number < answer }
	Higher
{:else if number > answer }
	Lower
{:else }
	Guess a Number
{/if}
</h1>
<input type="text" bind:value={number}>
```

## Each blocks
In case we want to loop through a list of data we use an Each block

```html
<script>
  let people = ["dustin", "fab", "ric", "emma"]
</script>

<ul>
	{#each people as person}
		<li>
			{person}
		</li>
	{/each}
</ul>
```

Links to REPLs: 

https://svelte.dev/repl/cae979145fa34396928a2fc207ba5530?version=3.16.0

https://svelte.dev/repl/2d12df9bf2e84030b2449703ff565318?version=3.16.0