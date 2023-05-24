<script>
    import {onDestroy} from "svelte";
    import {clickOutside} from '../utils/clickOutside.js';
    import NavLink from "./NavLink.svelte";
    import NavActions from "./NavActions.svelte";

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
        if (!isOpen) {
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
        <svg fill="none" viewBox="0 0 24 24" class="h-8 w-8" stroke="currentColor">
            <path d="M4 6h16M4 12h16M4 18h16" stroke-linecap="round" stroke-linejoin="round" class="inline-flex"
                  stroke-width="2"></path>
            <path d="M6 18L18 6M6 6l12 12" stroke-linecap="round" stroke-linejoin="round" class="hidden"
                  stroke-width="2"></path>
        </svg>
    </button>

    {#if isOpen}
        <div class="fixed inset-0 bg-gray-900 bg-opacity-60 z-50" on:click_outside={handleClickOutside}>
            <div class="nav-menu fixed inset-y-0 left-0 w-3/4 bg-white dark:bg-neutral-900 flex flex-col justify-between"
                 use:clickOutside
                 on:click_outside={handleClickOutside}>

                <div class="p-6 ">
                    <ul
                            class=" text-2xl  uppercase"
                    >
                        <NavLink on:click={handleClickOutside} href="/">Home</NavLink>

                        <NavLink on:click={handleClickOutside} href="/blog">Blog</NavLink>

                        <NavLink on:click={handleClickOutside} href="/about">About</NavLink>
                    </ul>
                </div>

                <NavActions/>

            </div>
        </div>
    {/if}
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
