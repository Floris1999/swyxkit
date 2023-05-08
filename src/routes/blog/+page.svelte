<script>
    // import { browser } from '$app/environment';
    // import { goto } from '$app/navigation';
    // import { page } from '$app/stores';
    import {queryParam, ssp} from 'sveltekit-search-params';

    import {SITE_TITLE, POST_CATEGORIES} from '$lib/siteConfig';

    import GridCard from "../../components/GridCard.svelte";

    /** @type {import('./$types').PageData} */
    export let data;

    // technically this is a slighlty different type because doesnt have 'content' but we'll let it slide
    /** @type {import('$lib/types').ContentItem[]} */
    $: items = data.items;

    // https://github.com/paoloricciuti/sveltekit-search-params#how-to-use-it
    /** @type import('svelte/store').Writable<String[] | null> */
    let selectedCategories = queryParam(
        'show',
        {
            encode: (arr) => arr?.toString(),
            decode: (str) => str?.split(',')?.filter((e) => e) ?? []
        },
        {debounceHistory: 500}
    );
    let search = queryParam('filter', ssp.string(), {
        debounceHistory: 500
    });

    let inputEl;

    function focusSearch(e) {
        if (e.key === '/' && inputEl) inputEl.select();
    }

    let items2 = [
        {
            canonical: "https://official-site.com/my-title",
            category: "blog",
            content: "\r\nmy great intro\r\n\r\n## my subtitle\r\n\r\nlorem ipsum ",
            date: "2023-04-22T00:00:00.000Z",
            description: "my great description ",
            frontmatter: {
                title: "my title",
                subtitle: "my great subtitle",
                description: "my great description",
                slug: "my-title",
                tags: ["foo", "bar", "baz"],
            },
            ghMetadata: {
                issueUrl: "https://github.com/Floris1999/swyxkit/issues/1",
                commentsUrl:
                    "https://api.github.com/repos/Floris1999/swyxkit/issues/1/comments",
                title: "Test",
                created_at: "2023-04-02T09:08:26Z",
                updated_at: "2023-04-02T09:10:07Z",
            },
            image: "https://my_image_url.com/img-4.png",
            readingTime: "1 minute",
            slug: "my-title",
            subtitle: "my great subtitle",
            tags: ["foo", "bar", "baz"],
            title: "my title",
            type: "blog",
        },
        {
            canonical: "https://official-site.com/my-title",
            category: "blog",
            content: "\r\nmy great intro\r\n\r\n## my subtitle\r\n\r\nlorem ipsum ",
            date: "2023-04-22T00:00:00.000Z",
            description: "my great description ",
            frontmatter: {
                title: "my great title",
                subtitle: "my great subtitle",
                description: "my great description",
                slug: "my-title",
                tags: ["foo", "bar", "baz"],
            },
            ghMetadata: {
                issueUrl: "https://github.com/Floris1999/swyxkit/issues/1",
                commentsUrl:
                    "https://api.github.com/repos/Floris1999/swyxkit/issues/1/comments",
                title: "Test",
                created_at: "2023-04-02T09:08:26Z",
                updated_at: "2023-04-02T09:10:07Z",
            },
            image: "https://my_image_url.com/img-4.png",
            readingTime: "1 minute",
            slug: "my-title",
            subtitle: "my great subtitle",
            tags: ["foo", "bar", "baz"],
            title: "my great title",
            type: "blog",
        },

        {
            canonical: "https://official-site.com/my-title",
            category: "blog",
            content: "\r\nmy great intro\r\n\r\n## my subtitle\r\n\r\nlorem ipsum ",
            date: "2023-04-22T00:00:00.000Z",
            description: "my great description ",
            frontmatter: {
                title: "my great title",
                subtitle: "my great subtitle",
                description: "my great description",
                slug: "my-title",
                tags: ["foo", "bar", "baz"],
            },
            ghMetadata: {
                issueUrl: "https://github.com/Floris1999/swyxkit/issues/1",
                commentsUrl:
                    "https://api.github.com/repos/Floris1999/swyxkit/issues/1/comments",
                title: "Test",
                created_at: "2023-04-02T09:08:26Z",
                updated_at: "2023-04-02T09:10:07Z",
            },
            image: "https://my_image_url.com/img-4.png",
            readingTime: "1 minute",
            slug: "my-title",
            subtitle: "my great subtitle",
            tags: ["foo", "bar", "baz"],
            title: "my great title",
            type: "blog",
        },

        {
            canonical: "https://official-site.com/my-title",
            category: "blog",
            content: "\r\nmy great intro\r\n\r\n## my subtitle\r\n\r\nlorem ipsum ",
            date: "2023-04-22T00:00:00.000Z",
            description: "my great description ",
            frontmatter: {
                title: "my great title",
                subtitle: "my great subtitle",
                description: "my great description",
                slug: "my-title",
                tags: ["foo", "bar", "baz"],
            },
            ghMetadata: {
                issueUrl: "https://github.com/Floris1999/swyxkit/issues/1",
                commentsUrl:
                    "https://api.github.com/repos/Floris1999/swyxkit/issues/1/comments",
                title: "Test",
                created_at: "2023-04-02T09:08:26Z",
                updated_at: "2023-04-02T09:10:07Z",
            },
            image: "https://my_image_url.com/img-4.png",
            readingTime: "1 minute",
            slug: "my-title",
            subtitle: "my great subtitle",
            tags: ["foo", "bar", "baz"],
            title: "my great title",
            type: "blog",
        },

        {
            canonical: "https://official-site.com/my-title",
            category: "blog",
            content: "\r\nmy great intro\r\n\r\n## my subtitle\r\n\r\nlorem ipsum ",
            date: "2023-04-22T00:00:00.000Z",
            description: "my great description ",
            frontmatter: {
                title: "my great title",
                subtitle: "my great subtitle",
                description: "my great description",
                slug: "my-title",
                tags: ["foo", "bar", "baz"],
            },
            ghMetadata: {
                issueUrl: "https://github.com/Floris1999/swyxkit/issues/1",
                commentsUrl:
                    "https://api.github.com/repos/Floris1999/swyxkit/issues/1/comments",
                title: "Test",
                created_at: "2023-04-02T09:08:26Z",
                updated_at: "2023-04-02T09:10:07Z",
            },
            image: "https://my_image_url.com/img-4.png",
            readingTime: "1 minute",
            slug: "my-title",
            subtitle: "my great subtitle",
            tags: ["foo", "bar", "baz"],
            title: "my great title",
            type: "blog",
        },
    ]

    // https://github.com/leeoniya/uFuzzy#options
    // we know this has js weight, but we tried lazyloading and it wasnt significant enough for the added complexity
    // https://github.com/sw-yx/swyxkit/pull/171
    // this will be slow if you have thousands of items, but most people don't
    let isTruncated = items?.length > 20;


    console.log(items2)

    // we are lazy loading a fuzzy search function
    // with a fallback to a simple filter function
    let loaded = false;
    const filterCategories = async (_items, _, s) => {
        if (!$selectedCategories?.length) return _items;
        return _items
            .filter((item) => {
                return $selectedCategories
                    .map((element) => {
                        return element.toLowerCase();
                    })
                    .includes(item.category.toLowerCase());
            })
            .filter((item) => item.toString().toLowerCase().includes(s));
    };
    $: searchFn = filterCategories;

    function loadsearchFn() {
        if (loaded) return;
        import('./fuzzySearch').then((fuzzy) => {
            searchFn = fuzzy.fuzzySearch;
            loaded = true;
        });
    }

    if ($search) loadsearchFn()
    /** @type import('$lib/types').ContentItem[]  */
    let list;
    $: searchFn(items, $selectedCategories, $search).then(_items => list = _items);

    // .slice(0, isTruncated ? 2 : items.length);
</script>

<svelte:head>
    <title>{SITE_TITLE} Blog Index</title>
    <meta name="description" content={`Latest ${SITE_TITLE} posts`}/>
</svelte:head>

<svelte:window on:keyup={focusSearch}/>

<section class="relative mx-auto flex w-full items-center border border-t-0 border-b-0 border-black 2xl:max-w-7xl dark:border-gray-600"
         aria-labelledby="feature-three" id="feature-three">
    <div class="grid h-40 grid-cols-3 grid-rows-6 gap-4 w-full">
        <div class="row-span-1 row-end-3 ">
            <h1 class="mb-4 text-3xl font-bold tracking-tight text-black dark:text-white md:text-5xl">
                {SITE_TITLE} Blog
            </h1>
        </div>
        <div class="col-start-1 col-end-7 row-start-7 bg-blue-500">
            <input
                    aria-label="Search articles"
                    type="text"
                    bind:value={$search}
                    bind:this={inputEl}
                    on:focus={loadsearchFn}
                    placeholder="Hit / to search"
                    class="block w-full border border-gray-200 bg-white px-4 py-2 h-full text-gray-900 focus:border-blue-500 focus:ring-blue-500 dark:border-gray-900 dark:bg-gray-800 dark:text-gray-100"
            />
        </div>
    </div>

</section>

<section class="relative flex w-full items-center border-y border-black dark:border-gray-600">
    <div class="relative mx-auto w-full items-center 2xl:max-w-7xl">
        <div class="grid grid-cols-1 divide-black border-black dark:border-gray-600 md:divide-x md:divide-y-0 lg:grid-cols-2 2xl:border-x">
            <div class="relative h-full items-center gap-12 p-8 lg:inline-flex lg:px-20">

            </div>
        </div>
    </div>
</section>

<section class="relative flex w-full items-center border-b border-black dark:border-gray-600">
    <div class="relative mx-auto w-full items-center divide-y-2 divide-black border-black 2xl:max-w-7xl 2xl:border-x dark:border-gray-600">
        {#if items2?.length}
            {#each items2.reduce((acc, item, i) => (i % 2 === 0 ? [...acc, [item]] : [...acc.slice(0, -1), [...acc.slice(-1)[0], item]]), []) as pair}
                <div class="grid grid-cols-1 divide-y divide-black md:grid-cols-2 md:divide-x-2 md:divide-y-0">
                    {#each pair as item}
                        <GridCard
                                href={item.slug}
                                title={item.title}
                                stringData={new Date(item.date).toISOString().slice(0, 10)}
                                ghMetadata={item.ghMetadata}
                                date={new Date(item.date)}
                        >
                            {item.description}
                        </GridCard>
                    {/each}
                </div>
            {/each}
        {/if}
    </div>
</section>


<!--<section class="relative mx-auto flex w-full items-center 2xl:max-w-7xl"-->
<!--         aria-labelledby="feature-three">-->
<!--    <div-->
<!--            class="relative mx-auto w-full items-center 2xl:max-w-7xl 2xl:px-0">-->
<!--        <div class="mt-16 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 lg:gap-12">-->
<!--            <a href="/posts/1" title=" Behind Flabbergasted New Design System"-->
<!--            >-->
<!--                <div class="shadow-large flex h-full flex-col divide-y-2 divide-black overflow-hidden border-2 border-black duration-200 hover:shadow-none">-->
<!--                    <div class="flex-shrink-0"><img alt=" Behind Flabbergasted New Design System"-->
<!--                                                    class="h-64 w-full object-cover" src="/images/switches.png"/>-->
<!--                    </div>-->
<!--                    <div class="flex flex-1 flex-col justify-between bg-white p-6">-->
<!--                        <div class="flex-1">-->
<!--                            <div class="flex space-x-1 text-sm text-black">-->
<!--                                <time datetime="Sat Jul 01">Sat Jul 01</time>-->
<!--                                <span aria-hidden="true">·</span> <span>By Matto Smitho</span></div>-->
<!--                            <div class="mt-2 block">-->
<!--                                <p class="text-xl text-black lg:text-3xl">Behind Flabbergasted New Design System</p>-->
<!--                                <p class="mt-3 text-xl text-black">The story of our site-wide redesign and web tech-->
<!--                                    and accessibility wins.</p>-->
<!--                            </div>-->
<!--                        </div>-->
<!--                    </div>-->
<!--                </div>-->
<!--            </a-->
<!--            ><a href="/posts/2"-->
<!--                title="How to use Flabbergasted free email marketing to build an audience &amp; generate sales"-->
<!--        >-->
<!--            <div class="shadow-large flex h-full flex-col divide-y-2 divide-black overflow-hidden border-2 border-black duration-200 hover:shadow-none">-->
<!--                <div class="flex-shrink-0"><img-->
<!--                        alt="How to use Flabbergasted free email marketing to build an audience &amp; generate sales"-->
<!--                        class="h-64 w-full object-cover" src="/images/balls.png"/></div>-->
<!--                <div class="flex flex-1 flex-col justify-between bg-white p-6">-->
<!--                    <div class="flex-1">-->
<!--                        <div class="flex space-x-1 text-sm text-black">-->
<!--                            <time datetime="Sat Jul 08">Sat Jul 08</time>-->
<!--                            <span aria-hidden="true">·</span> <span>By Brado Pitto</span></div>-->
<!--                        <div class="mt-2 block">-->
<!--                            <p class="text-xl text-black lg:text-3xl">How to use Flabbergasted free email marketing-->
<!--                                to build an audience &amp; generate sales</p>-->
<!--                            <p class="mt-3 text-xl text-black">Learn how creators can build an audience and generate-->
<!--                                more sales using Gumroad's built-in, free email marketing tool.</p>-->
<!--                        </div>-->
<!--                    </div>-->
<!--                </div>-->
<!--            </div>-->
<!--        </a-->
<!--        ><a href="/posts/3" title="How to earn a side income selling digital products"-->
<!--        >-->
<!--            <div class="shadow-large flex h-full flex-col divide-y-2 divide-black overflow-hidden border-2 border-black duration-200 hover:shadow-none">-->
<!--                <div class="flex-shrink-0"><img alt="How to earn a side income selling digital products"-->
<!--                                                class="h-64 w-full object-cover" src="/images/checkboxes.png"/>-->
<!--                </div>-->
<!--                <div class="flex flex-1 flex-col justify-between bg-white p-6">-->
<!--                    <div class="flex-1">-->
<!--                        <div class="flex space-x-1 text-sm text-black">-->
<!--                            <time datetime="Sat Jul 15">Sat Jul 15</time>-->
<!--                            <span aria-hidden="true">·</span> <span>By Akihiro Suzuki</span></div>-->
<!--                        <div class="mt-2 block">-->
<!--                            <p class="text-xl text-black lg:text-3xl">How to earn a side income selling digital-->
<!--                                products</p>-->
<!--                            <p class="mt-3 text-xl text-black">A whole new world of potential revenue streams await-->
<!--                                you and getting started is easier than you think. In fact, your greatest monetary-->
<!--                                gains may be the easiest you’ve ever made.</p>-->
<!--                        </div>-->
<!--                    </div>-->
<!--                </div>-->
<!--            </div>-->
<!--        </a-->
<!--        ><a href="/posts/4" title="53 free Procreate brushes you can download on Flabbergasted"-->
<!--        >-->
<!--            <div class="shadow-large flex h-full flex-col divide-y-2 divide-black overflow-hidden border-2 border-black duration-200 hover:shadow-none">-->
<!--                <div class="flex-shrink-0"><img alt="53 free Procreate brushes you can download on Flabbergasted"-->
<!--                                                class="h-64 w-full object-cover" src="/images/buttons.png"/></div>-->
<!--                <div class="flex flex-1 flex-col justify-between bg-white p-6">-->
<!--                    <div class="flex-1">-->
<!--                        <div class="flex space-x-1 text-sm text-black">-->
<!--                            <time datetime="Tue Aug 08">Tue Aug 08</time>-->
<!--                            <span aria-hidden="true">·</span> <span>By Munehide Hamataka</span></div>-->
<!--                        <div class="mt-2 block">-->
<!--                            <p class="text-xl text-black lg:text-3xl">53 free Procreate brushes you can download on-->
<!--                                Flabbergasted</p>-->
<!--                            <p class="mt-3 text-xl text-black">Download 53 Procreate Brushes from top Flabbergasted-->
<!--                                creators and take your illustration art to the next level!</p>-->
<!--                        </div>-->
<!--                    </div>-->
<!--                </div>-->
<!--            </div>-->
<!--        </a-->
<!--        >-->
<!--        </div>-->
<!--    </div>-->
<!--</section>-->

<!--<section class="relative mx-auto flex w-full items-center border-2 border-t-0 border-black 2xl:max-w-7xl"-->
<!--         aria-labelledby="feature-three" id="feature-three">-->
<!--    {#if items2?.length}-->
<!--        <GridWithSlot height={items2.length * 400}>-->
<!--            {#each items2 as item, i}-->
<!--                <GridCard-->
<!--                        gridArea="grid-area: {1 + (i * 5)} / 2 / {5 + (i * 5)} / 8;"-->
<!--                        href={item.slug}-->
<!--                        title={item.title}-->
<!--                        stringData={new Date(item.date).toISOString().slice(0, 10)}-->
<!--                        ghMetadata={item.ghMetadata}-->
<!--                        {item}-->
<!--                >-->
<!--                    {#if item.highlightedResults}-->
<!--    						<span class="italic">-->
<!--    							{@html item.highlightedResults}-->
<!--    						</span>-->
<!--                    {:else}-->
<!--                        {item.description}-->
<!--                    {/if}-->
<!--                </GridCard>-->
<!--            {/each}-->
<!--        </GridWithSlot>-->
<!--    {/if}-->
<!--</section>-->

<!--<section class="mx-auto flex max-w-4xl w-full flex-col items-start justify-center ">-->
<!--    <GridWithSlot height=300>-->
<!--        <div style="grid-area: 1 / 1 / 3 / 9;">-->
<!--            <h1 class="mb-4 text-3xl font-bold tracking-tight text-black dark:text-white md:text-5xl">-->
<!--                {SITE_TITLE} Blog-->
<!--            </h1>-->
<!--        </div>-->

<!--        <div style="grid-area: 5 / 1 / 6 / last-line;">-->
<!--            <input-->
<!--                    aria-label="Search articles"-->
<!--                    type="text"-->
<!--                    bind:value={$search}-->
<!--                    bind:this={inputEl}-->
<!--                    on:focus={loadsearchFn}-->
<!--                    placeholder="Hit / to search"-->
<!--                    class="block w-full border border-gray-200 bg-white px-4 py-2 h-full text-gray-900 focus:border-blue-500 focus:ring-blue-500 dark:border-gray-900 dark:bg-gray-800 dark:text-gray-100"-->
<!--            />-->
<!--            <svg-->
<!--                    class="absolute right-3 top-3 h-5 w-5 text-gray-400 dark:text-gray-300"-->
<!--                    xmlns="http://www.w3.org/2000/svg"-->
<!--                    fill="none"-->
<!--                    viewBox="0 0 24 24"-->
<!--                    stroke="currentColor"-->
<!--            >-->
<!--                <path-->
<!--                        stroke-linecap="round"-->
<!--                        stroke-linejoin="round"-->
<!--                        stroke-width="2"-->
<!--                        d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"-->
<!--                />-->
<!--            </svg-->
<!--            >-->
<!--        </div>-->
<!--    </GridWithSlot>-->


<!--&lt;!&ndash;    <GridWithSlot height=300>&ndash;&gt;-->
<!--&lt;!&ndash;    </GridWithSlot>&ndash;&gt;-->


<!--    &lt;!&ndash;    &lt;!&ndash; if you have multiple categories enabled &ndash;&gt;&ndash;&gt;-->
<!--    &lt;!&ndash;{#if POST_CATEGORIES.length > 1}&ndash;&gt;-->
<!--    &lt;!&ndash;    <div class="mt-2 mb-8 flex items-center">&ndash;&gt;-->
<!--    &lt;!&ndash;        <div class="mr-2 text-gray-900 dark:text-gray-400">Filter:</div>&ndash;&gt;-->
<!--    &lt;!&ndash;        <div class="grid grid-cols-2 rounded-md shadow-sm sm:grid-cols-2">&ndash;&gt;-->
<!--    &lt;!&ndash;            {#each POST_CATEGORIES as availableCategory}&ndash;&gt;-->
<!--    &lt;!&ndash;                <div>&ndash;&gt;-->
<!--    &lt;!&ndash;                    <input&ndash;&gt;-->
<!--    &lt;!&ndash;                            id="category-{availableCategory}"&ndash;&gt;-->
<!--    &lt;!&ndash;                            class="peer sr-only"&ndash;&gt;-->
<!--    &lt;!&ndash;                            type="checkbox"&ndash;&gt;-->
<!--    &lt;!&ndash;                            bind:group={$selectedCategories}&ndash;&gt;-->
<!--    &lt;!&ndash;                            value={availableCategory}&ndash;&gt;-->
<!--    &lt;!&ndash;                    />&ndash;&gt;-->
<!--    &lt;!&ndash;                    <label&ndash;&gt;-->
<!--    &lt;!&ndash;                            for="category-{availableCategory}"&ndash;&gt;-->
<!--    &lt;!&ndash;                            class="inline-flex w-full cursor-pointer items-center justify-between border border-gray-200 bg-white px-4 py-2 text-gray-500 hover:bg-gray-100 hover:text-gray-600 peer-checked:border-purple-600 peer-checked:text-purple-600 dark:border-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-gray-300 dark:peer-checked:text-purple-500"&ndash;&gt;-->
<!--    &lt;!&ndash;                    >&ndash;&gt;-->
<!--    &lt;!&ndash;                        {availableCategory}&ndash;&gt;-->
<!--    &lt;!&ndash;                    </label>&ndash;&gt;-->
<!--    &lt;!&ndash;                </div>&ndash;&gt;-->
<!--    &lt;!&ndash;            {/each}&ndash;&gt;-->
<!--    &lt;!&ndash;        </div>&ndash;&gt;-->
<!--    &lt;!&ndash;    </div>&ndash;&gt;-->
<!--    &lt;!&ndash;{/if}&ndash;&gt;-->


<!--    &lt;!&ndash;{#if list?.length}&ndash;&gt;-->
<!--    &lt;!&ndash;    <ul class="">&ndash;&gt;-->
<!--    &lt;!&ndash;        {#each list as item}&ndash;&gt;-->
<!--    &lt;!&ndash;            <li class="mb-8 text-lg">&ndash;&gt;-->
<!--    &lt;!&ndash;                &lt;!&ndash; <code class="mr-4">{item.data.date}</code> &ndash;&gt;&ndash;&gt;-->
<!--    &lt;!&ndash;                <IndexCard&ndash;&gt;-->
<!--    &lt;!&ndash;                        href={item.slug}&ndash;&gt;-->
<!--    &lt;!&ndash;                        title={item.title}&ndash;&gt;-->
<!--    &lt;!&ndash;                        stringData={new Date(item.date).toISOString().slice(0, 10)}&ndash;&gt;-->
<!--    &lt;!&ndash;                        ghMetadata={item.ghMetadata}&ndash;&gt;-->
<!--    &lt;!&ndash;                        {item}&ndash;&gt;-->
<!--    &lt;!&ndash;                >&ndash;&gt;-->
<!--    &lt;!&ndash;                    {#if item.highlightedResults}&ndash;&gt;-->
<!--	&lt;!&ndash;						<span class="italic">&ndash;&gt;-->
<!--	&lt;!&ndash;							{@html item.highlightedResults}&ndash;&gt;-->
<!--	&lt;!&ndash;						</span>&ndash;&gt;-->
<!--    &lt;!&ndash;                    {:else}&ndash;&gt;-->
<!--    &lt;!&ndash;                        {item.description}&ndash;&gt;-->
<!--    &lt;!&ndash;                    {/if}&ndash;&gt;-->
<!--    &lt;!&ndash;                </IndexCard>&ndash;&gt;-->
<!--    &lt;!&ndash;            </li>&ndash;&gt;-->
<!--    &lt;!&ndash;        {/each}&ndash;&gt;-->
<!--    &lt;!&ndash;    </ul>&ndash;&gt;-->
<!--    &lt;!&ndash;    {#if isTruncated}&ndash;&gt;-->
<!--    &lt;!&ndash;        <div class="flex justify-center">&ndash;&gt;-->
<!--    &lt;!&ndash;            <button&ndash;&gt;-->
<!--    &lt;!&ndash;                    on:click={() => (isTruncated = false)}&ndash;&gt;-->
<!--    &lt;!&ndash;                    class="inline-block rounded bg-blue-100 p-4 text-lg font-bold tracking-tight text-black hover:text-yellow-900 dark:bg-blue-900 dark:text-white hover:dark:text-yellow-200 md:text-2xl"&ndash;&gt;-->
<!--    &lt;!&ndash;            >&ndash;&gt;-->
<!--    &lt;!&ndash;                Load More Posts...&ndash;&gt;-->
<!--    &lt;!&ndash;            </button>&ndash;&gt;-->
<!--    &lt;!&ndash;        </div>&ndash;&gt;-->
<!--    &lt;!&ndash;    {/if}&ndash;&gt;-->
<!--    &lt;!&ndash;{:else if $search}&ndash;&gt;-->
<!--    &lt;!&ndash;    <div class="prose dark:prose-invert">&ndash;&gt;-->
<!--    &lt;!&ndash;        No posts found for&ndash;&gt;-->
<!--    &lt;!&ndash;        <code>{$search}</code>.&ndash;&gt;-->
<!--    &lt;!&ndash;    </div>&ndash;&gt;-->
<!--    &lt;!&ndash;    <button class="bg-slate-500 p-2" on:click={() => ($search = '')}>Clear your search</button>&ndash;&gt;-->
<!--    &lt;!&ndash;{:else}&ndash;&gt;-->
<!--    &lt;!&ndash;    <div class="prose dark:prose-invert">No blogposts found!</div>&ndash;&gt;-->
<!--    &lt;!&ndash;{/if}&ndash;&gt;-->
<!--</section>-->
