<script>
	import { onDestroy } from "svelte";
	import {clickOutside} from '../utils/clickOutside.js';

	let isOpen = false;
	let handleClick = null;
	function removeClickListener() {
		if (handleClick) {
			document.removeEventListener("click", handleClick);
			handleClick = null;
		}
	}

	function handleClickOutside(event) {
		if (isOpen && !event.target.closest(".nav-close-div")) {
			isOpen = false;
		}
	}

	function toggleMenu() {
		isOpen = !isOpen;
		if (isOpen) {
			// addClickListener();
		} else {
			removeClickListener();
		}
	}

	onDestroy(() => {
		removeClickListener();
	});
</script>

<div class="ml-[-0.60rem] md:hidden">
	<button
		class="focus:shadow-outline ml-auto border-2 border-black bg-red-500 focus:outline-none md:hidden"
		aria-label="Toggle menu"
		type="button"
		on:click={toggleMenu}
	>
		{#if !isOpen}
			<svg fill="none" viewBox="0 0 24 24" class="h-8 w-8" stroke="currentColor">
				<path d="M4 6h16M4 12h16M4 18h16" stroke-linecap="round" stroke-linejoin="round" class="inline-flex"
					  stroke-width="2"></path>
				<path d="M6 18L18 6M6 6l12 12" stroke-linecap="round" stroke-linejoin="round" class="hidden"
					  stroke-width="2"></path>
			</svg>
		{/if}
	</button>

	{#if isOpen}
		<div class="fixed inset-0 bg-gray-900 bg-opacity-50 z-50" on:click_outside={handleClickOutside}>
			<div class="nav-menu fixed inset-y-0 left-0 w-3/4 bg-gray-800 p-6" use:clickOutside on:click_outside={handleClickOutside}>
				<ul
						class=" text-2xl  uppercase"
				>
					<li
							class="border-b border-gray-300 font-semibold text-gray-900 dark:border-gray-700 dark:text-gray-100"
							style="transition-delay: 150ms;"
					>
						<a
								class="flex w-auto pb-4"
								on:click={() => setTimeout(() => (isOpen = false), 300)}
								href="/">Home</a
						>
					</li>
					<li
							class="border-b border-gray-300 font-semibold text-gray-900 dark:border-gray-700 dark:text-gray-100"
							style="transition-delay: 250ms;"
					>
						<a
								class="flex w-auto pb-4"
								on:click={() => setTimeout(() => (isOpen = false), 300)}
								href="/blog">Blog</a
						>
					</li>
					<li
							class="border-b border-gray-300 font-semibold text-gray-900 dark:border-gray-700 dark:text-gray-100"
							style="transition-delay: 350ms;"
					>
						<a
								class="flex w-auto pb-4"
								on:click={() => setTimeout(() => (isOpen = false), 300)}
								href="/about">About</a
						>
					</li>
					<li
							class="border-b border-gray-300 font-semibold text-gray-900 dark:border-gray-700 dark:text-gray-100"
							style="transition-delay: 400ms;"
					>
						<a
								class="flex w-auto pb-4"
								on:click={() => setTimeout(() => (isOpen = false), 300)}
								href="https://github.com/sw-yx/swyxkit">GitHub</a
						>
					</li>
				</ul>

			</div>
		</div>
	{/if}
	<!--{#if false}-->
		<ul
			class="menu absolute flex flex-col bg-gray-50 text-2xl  uppercase dark:bg-gray-900"
		>
			<li
				class="border-b border-gray-300 font-semibold text-gray-900 dark:border-gray-700 dark:text-gray-100"
				style="transition-delay: 150ms;"
			>
				<a
					class="flex w-auto pb-4"
					on:click={() => setTimeout(() => (isOpen = false), 300)}
					href="/">Home</a
				>
			</li>
			<li
				class="border-b border-gray-300 font-semibold text-gray-900 dark:border-gray-700 dark:text-gray-100"
				style="transition-delay: 250ms;"
			>
				<a
					class="flex w-auto pb-4"
					on:click={() => setTimeout(() => (isOpen = false), 300)}
					href="/blog">Blog</a
				>
			</li>
			<li
				class="border-b border-gray-300 font-semibold text-gray-900 dark:border-gray-700 dark:text-gray-100"
				style="transition-delay: 350ms;"
			>
				<a
					class="flex w-auto pb-4"
					on:click={() => setTimeout(() => (isOpen = false), 300)}
					href="/about">About</a
				>
			</li>
			<li
				class="border-b border-gray-300 font-semibold text-gray-900 dark:border-gray-700 dark:text-gray-100"
				style="transition-delay: 400ms;"
			>
				<a
					class="flex w-auto pb-4"
					on:click={() => setTimeout(() => (isOpen = false), 300)}
					href="https://github.com/sw-yx/swyxkit">GitHub</a
				>
			</li>
			<!-- <li
			class="border-b border-gray-300 dark:border-gray-700 text-gray-900 dark:text-gray-100 font-semibold"
			style="transition-delay: 325ms;"
		>
			<a class="flex w-auto pb-4" on:click={() => setTimeout(() => isOpen = false, 200)} href="/tweets">Tweets</a>
		</li> -->
		</ul>
	<!--{/if}-->
</div>

<style lang="postcss">
	.burger {
		transition: opacity 300ms ease;
		border: 0;
		background: transparent;
		width: 40px;
		height: 40px;
		position: relative;
	}

	.burger svg {
		transform: translate(-50%, -50%) scale(1);
		top: 50%;
		left: 50%;
		opacity: 1;
		transition: opacity 300ms ease, transform 300ms ease;
	}

	.menu {
		padding: 0 28px 0 4px;
		margin: 0;
		padding-top: 24px;
		width: 100%;
		height: 100vh;
		z-index: 1000;
		opacity: 0;
		left: 0;
		transition: opacity 300ms ease, transform 300ms ease;
	}

	.menu li {
		transform: translateX(-16px);
		opacity: 0;
		transition: opacity 300ms ease, transform 300ms ease, width 300ms ease, border-color 300ms ease;
		width: 0px;
		white-space: nowrap;
	}

	.menuRendered {
		opacity: 1;
	}

	.menuRendered li {
		@apply w-full border-gray-200 dark:border-gray-600;
		transform: translateX(0);
		opacity: 1;
	}

	.menu > * + * {
		margin-top: 24px;
	}

	@keyframes grow {
		0% {
			height: 0px;
		}
		100% {
			height: 24px;
		}
	}
</style>
