<script>
	import Button from '$lib/Button.svelte';
	import TableComponent from '$lib/Table.svelte';
	import DynamicComponent from '$lib/Dynamic.svelte';
	let label = 'Click Me!';
	let classStyle = 'btn btn-custom';

	let data = [
		{ name: 'John Doe', email: 'john@email.com', phone: '+91846665646', designation: 'Engineer' },
		{
			name: 'Jane Smith',
			email: 'jane@email.com',
			phone: '+91886665656',
			designation: 'Developer'
		},
		{ name: 'Sam Wilson', email: 'sam@email.com', phone: '+91816665656', designation: 'Manager' }
	];
	let customAttributes = {
		label: 'Hello',
		classStyle: 'btn btn-dynamic'
	};
</script>

<h1>Welcome to your library project</h1>
<p>Create your package using @sveltejs/package and preview/showcase your work with SvelteKit</p>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<hr />
<p>1. This is testing button which is render by library</p>

<Button {classStyle} {label} />
<hr />

<p>2. This is testing Table which is render by library</p>
<TableComponent tableData={data} />
<hr />

<DynamicComponent component={Button} {...customAttributes} />
