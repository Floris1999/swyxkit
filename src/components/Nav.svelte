<script>
    import MobileMenu from './MobileMenu.svelte';
    import {REPO_URL} from '$lib/siteConfig';
    import NavLink from './NavLink.svelte';
    import NavActions from "./NavActions.svelte";


</script>

<div class="mx-auto flex w-full flex-col px-8 py-6 md:px-0 md:py-0 lg:flex-row lg:items-center lg:justify-between 2xl:max-w-7xl">
    <div class="flex flex-row items-center justify-between text-black">
        <a class="inline-flex items-center gap-3 text-lg font-bold tracking-tighter text-black md:hidden"
           href="/"><span>Floris.</span> </a
        >
        <MobileMenu/>
    </div>
    <nav class="hidden flex-grow flex-col items-center px-5 py-2 md:mt-0 md:flex md:flex-row md:justify-start md:px-0 md:py-0 md:pb-0 lg:p-0">

        <NavLink href="/">Home</NavLink>

        <NavLink href="/blog">Blog</NavLink>

        <NavLink href="/about">About</NavLink>

        <NavActions/>
<!--        <a-->
<!--            class="hover:bg-lila-900 hover:text-lila-500 text-lila-500 inline-flex transform items-center justify-center border-l-2 border-black bg-black px-6 py-2 text-center text-lg transition duration-500 ease-in-out focus:outline-none focus:ring-2 focus:ring-red-500 focus:ring-offset-2 md:ml-auto md:py-8"-->
<!--            href="https://lexingtonthemes.lemonsqueezy.com/checkout/buy/645ac44b-ee66-4368-bb58-be869569fb88"><span>Buy Flabbergasted for $69</span></a>-->
    </nav>
</div>

