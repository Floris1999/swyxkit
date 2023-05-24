<script>
    import '../tailwind.css';
    import Nav from '../components/Nav.svelte';
    import {CHESS_PROFILE, LINKEDIN, MY_TWITTER_HANDLE, REPO_OWNER, REPO_URL, SITE_TITLE} from '$lib/siteConfig';
</script>

<svelte:head>
    <link
            rel="alternate"
            type="application/rss+xml"
            title={'RSS Feed for ' + SITE_TITLE}
            href="/rss.xml"
    />
</svelte:head>

<div class="sticky top-0 z-20 mx-auto w-full justify-center border-y border-black 2xl:max-w-7xl 2xl:border bg-white dark:bg-neutral-900 dark:border-gray-600"
     aria-labelledby="nav" id="nav">
    <Nav/>
</div>

<slot/>

<footer class="mx-auto mb-8 flex w-full max-w-2xl flex-col items-start justify-center">
    <hr class="border-1 mb-8 w-full border-gray-200 dark:border-gray-800"/>
    <div class="grid w-full max-w-2xl grid-cols-1 gap-4 px-4 pb-16 sm:grid-cols-2 sm:px-8">
        <div class="flex flex-col space-y-4">
            <a class="text-gray-500 transition hover:text-gray-300" href="/">Home</a>
            <a class="text-gray-500 transition hover:text-gray-300" href="/blog">Blog</a>
            <a class="text-gray-500 transition hover:text-gray-300" href="/about">About</a>
        </div>
        <div class="flex flex-col space-y-4">
            <a
                    class="text-gray-500 transition hover:text-gray-300"
                    target="_blank"
                    rel="noopener noreferrer"
                    href={'https://twitter.com/intent/follow?screen_name=' + MY_TWITTER_HANDLE}
            >
                Twitter
            </a>
            <a
                    class="text-gray-500 transition hover:text-gray-300"
                    target="_blank"
                    rel="noopener noreferrer"
                    href={'https://github.com/' + REPO_OWNER}
            >
                GitHub
            </a>

            <a
                    class="text-gray-500 transition hover:text-gray-300"
                    target="_blank"
                    rel="noopener noreferrer"
                    href={LINKEDIN}
            >
                LinkedIn
            </a>

            <a
                    class="text-gray-500 transition hover:text-gray-300"
                    target="_blank"
                    rel="noopener noreferrer"
                    href={CHESS_PROFILE}
            >
                Chess acount
            </a>


        </div>
    </div>
    <p class="prose px-4 dark:prose-invert sm:px-8">
        This blog is made with SvelteKit x Tailwind
    </p>
</footer>
