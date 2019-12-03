[Go back to README?](./README.md)
# Introduction

## Main Component
* Introduce basic Svelte concepts
  * variables (declaration, Svelte variable notation)
  * importing components
* Slot element in imported component
  * can contain html or other components
* Passing props to a component
```html
<script>
	import Parent from './Parent.svelte'
	import Child from './Child.svelte'
	let name = 'Bob'
</script>

<h1>Hello {name}</h1>

<Child />

<Parent myName="Bob">
	<p>paragraph in the main component</p>	
	<Child />
</Parent>
```

## Child Component
* Creating a basic component, using only HTML
```html
<p>I am in a different file!</p>
```

## Parent Component
* Using the `slot` element
* CSS written in this component will be scoped to this component
  * will not affect styles of any other components or parts of the app
* Variables as props need to be exported
  * this allows the variable to be declared when the component is called
```html
<script>
	export let myName;
</script>

<div>
	<p>
		Hello again {myName}
	</p>
	<slot></slot>
</div>

<style>
	div{
		background-color:pink;
		padding: 20px;
	}
</style>
```

Link To REPL:
  * [Live Introduction](https://svelte.dev/repl/c62c483eb229400ea3e33914a6656d21?version=3.16.0)
