[Go back to README?](./README.md)
# Other Features

## HTML in SVELTE
* Svelte allows for strings of markup to be converted into html with ease using the `@html` prefix

```html
<!-- Other features that people wish they had -->
<script>
	let string = `this string contains some <strong>HTML!!!</strong>`;
</script>

<p>{@html string}</p>
```
## Truly Reactive
* Svelte has the ability to make variables know to watch for variable changes without any complex state management systems or explicitly stating that the value should update
* Use of `JavaScript Labels` to create this neat trick. `:` is actually, believe it or not, vanilla JavaScript

```html
<!-- Other features that people wish they had -->
<script>
	let count = 0;
	$: doubled = count * 2;
	
	function handleClick() {
		count++
	}
	$: console.log(`the count is ${count} doubled is ${doubled}`);

</script>
<button on:click={handleClick}>
	Count: {count}
</button>
```

Link To REPL:

https://svelte.dev/repl/6622d035e4a34c22a5a13652bb520850?version=3.16.0 