---
title: Snippets
---

Just like elements can have children...

```html
/// no-file
<div>
	<p>I'm a child of the div</p>
</div>
```

...so can components. Before a component can accept children, though, it needs to know where to put them. We do this with the `children` prop and the render tag `{@render children()}` – which is a bit like a function call. Put this inside `Card.svelte`:

```svelte
/// file: Card.svelte
+++<script>+++
+++	const { children } = $props();+++
+++</script>+++
<div class="card">
	+++{@render children()}+++
</div>
```

You can now put things on the card:

```svelte
/// file: App.svelte
<Card>
	+++<span>Patrick BATEMAN</span>+++
	+++<span>Vice President</span>+++
</Card>
```
