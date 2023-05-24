<script>
    // import { browser } from '$app/environment';
    // import { goto } from '$app/navigation';
    // import { page } from '$app/stores';
    import {queryParam, ssp} from 'sveltekit-search-params';

    import {SITE_TITLE, POST_CATEGORIES} from '$lib/siteConfig';

    import GridCard from "../../components/GridCard.svelte";
    import hero from "$lib/assets/PXL_20220717_142943888.MP.jpg";
    import IndexCard from "../../components/IndexCard.svelte";

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
<section class="relative flex w-full items-center border-black dark:border-gray-600 border-b-0"
         aria-labelledby="feature-one"
         id="feature-one">
    <div class="relative mx-auto w-full items-center 2xl:max-w-7xl">
        <div class="grid grid-cols-1 divide-y-0 divide-black dark:divide-gray-600 border-black dark:border-gray-600 md:divide-x md:divide-y-0 lg:grid-cols-2 2xl:border-x">
            <div class="relative h-full items-center gap-12 p-8 lg:inline-flex lg:px-20">
                <div class="mx-auto max-w-xl text-left md:text-center lg:text-left">
                    <div>
                        <p class="mt-3 text-5xl tracking-tight text-black dark:text-white lg:text-7xl mb-2">Floris
                            Wieringa Blog
                        </p>


                    </div>

                    <div class="mt-10 flex flex-col gap-3 sm:flex-row">
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
            </div>
            <div class="bg-lila-500 block h-100 lg:mt-0 p-4">

            </div>
        </div>
    </div>
</section>

<!--<section class="relative mx-auto flex w-full items-center border border-t-0 border-b-0 border-black 2xl:max-w-7xl dark:border-gray-600"-->
<!--         aria-labelledby="feature-three" id="feature-three">-->
<!--    <div class="grid h-40 grid-cols-3 grid-rows-6 gap-4 w-full">-->
<!--        <div class="row-span-1 row-end-3 ">-->
<!--            <h1 class="mb-4 text-3xl font-bold tracking-tight text-black dark:text-white md:text-5xl">-->
<!--                {SITE_TITLE} Blog-->
<!--            </h1>-->
<!--        </div>-->
<!--        <div class="col-start-1 col-end-7 row-start-7 bg-blue-500">-->

<!--        </div>-->
<!--    </div>-->

<!--</section>-->

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
        {#if list?.length}
            {#each list.reduce((acc, item, i) => (i % 2 === 0 ? [...acc, [item]] : [...acc.slice(0, -1), [...acc.slice(-1)[0], item]]), []) as pair}
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

            {#if isTruncated}
                <div class="flex justify-center">
                    <button
                            on:click={() => (isTruncated = false)}
                            class="inline-flex w-full transform items-center justify-center rounded-xl border-2 border-black bg-white px-6 py-3 text-center text-black shadow-[5px_5px_black] transition duration-200 ease-in-out hover:bg-black hover:text-white hover:shadow-none focus:outline-none lg:w-auto dark:bg-gray-700 dark:hover:bg-gray-900"
                    >
                        Load More Posts...
                    </button>
                </div>
            {/if}
        {:else if $search}
            <div class="prose dark:prose-invert">
                No posts found for
                <code>{$search}</code>.
            </div>
            <button class="bg-slate-500 p-2" on:click={() => ($search = '')}>Clear your search</button>
        {:else}
            <div class="prose dark:prose-invert">No blogposts found!</div>
        {/if}

    </div>
</section>
