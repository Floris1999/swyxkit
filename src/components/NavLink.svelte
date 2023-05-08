<script>
	import { page } from '$app/stores';
	$: isActive = $page.url.pathname === $$props.href;
	export let href;
</script>

<a
	class="focus:text-orange/90 hover:text-lila-900 transform px-4 py-2 text-lg text-black transition duration-1000 ease-in-out focus:shadow-none focus:outline-none md:my-0"
	class:font-semibold={isActive}
	{href}
	><span class="capsize"><slot /> </span>
</a>
