<script>
	import '../app.postcss';
	export let style = "default"
	export let placeholder = "Enter email"
</script>

{#if style=="default"}
	<label class="block">
		<span class="ml-5 mt-5 block text-md font-large text-slate-900">Email</span>
		<input type=text value={placeholder} class="ml-5 mb-5 rounded-md border-1 border-gray-300 
		focus:outline-none focus:border-indigo-700 focus:ring-1 focus:ring-indigo-700">
	</label>
{/if}

{#if style=="invalid"}
	<label class="block">
		<span class="ml-5 block text-md font-large text-slate-900">Email</span>
		<input type=text value={placeholder} class="ml-5 mb-5 rounded-md border-1 border-red-500 text-red-500
		focus:outline-none focus:border-red-500 focus:ring-1 focus:ring-red-500">
	</label>
{/if}

{#if style=="disabled"}
	<label class="block">
		<span class="ml-5 block text-md font-large text-slate-900">Email</span>
		<input disabled type=text value={placeholder} class="ml-5 mb-5 rounded-md border-1 border-none bg-gray-200 text-gray-500">
	</label>
{/if}

<slot />
