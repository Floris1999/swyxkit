<script>
    // href={item.slug} title={item.data.title} date={item.data.date}
    export let href = '#';
    /** @type {import('$lib/types').ContentItem} */
    export let item = undefined;
    /** @type {import('$lib/types').GHMetadata} */
    export let ghMetadata = null;
    export let title = 'Untitled post';
    /** @type {string} */
    export let stringData = 'no date';
    export let date = null
    const months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']
</script>

<div class="group grid grid-cols-1 divide-y-2 divide-black">
    <a href={href} title=" Behind Flabbergasted New Design System">
        <article class="flex transition hover:bg-orange-600">
            <div class="rotate-180 p-2 [writing-mode:_vertical-lr] ">
                <time
                        datetime={date.toString()}
                        class="flex items-center justify-between gap-4 text-xs font-bold uppercase text-gray-900 dark:text-white"
                >
                    <span>{date.getFullYear()}</span>
                    <span class="w-px flex-1 bg-gray-900/10"></span>
                    <span>{months[date.getMonth()]} {date.getDate()}</span>
                </time>
            </div>

            <div class="flex flex-1 flex-col justify-between">
                <div class="border-s border-gray-900/10 p-4 sm:border-l-transparent sm:p-6">
                    <a href="#">
                        <h3 class="font-bold uppercase text-gray-900 dark:text-white">
                            {title}
                        </h3>
                    </a>

                    <p class="text-gray-600 mb-2 break-all sm:break-words dark:text-gray-400 hover:text-yellow-600 dark:hover:text-yellow-100">
                        <slot />
                    </p>

                    {#if item?.readingTime}
                        <p class="hidden sm:inline-block">{item?.readingTime}</p>
                    {/if}


                </div>
                <div class="sm:flex sm:items-end sm:justify-end">
                    <a
                            href="#"
                            class="block bg-yellow-300 px-5 py-3 text-center text-xs font-bold uppercase text-gray-900 transition hover:bg-yellow-400 group-hover:bg-gray-900"
                    >

                        <svg role="img" height="16" width="16" aria-hidden="true" viewBox="0 0 16 16"
                             data-encore-id="icon" class="group-hover:fill-white">
                            <path d="M7.19 1A.749.749 0 0 1 8.47.47L16 7.99l-7.53 7.521a.75.75 0 0 1-1.234-.815.75.75 0 0 1 .174-.243l5.72-5.714H.75a.75.75 0 1 1 0-1.498h12.38L7.41 1.529a.749.749 0 0 1-.22-.53z"></path>
                        </svg>
                    </a>
                </div>
            </div>
        </article>
    </a>
</div>

<!--<a style={gridArea} {href}-->
<!--   class="block p-6 bg-white border border-gray-200 shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">-->
<!--    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{title}</h5>-->
<!--    <p class="text-gray-600 mb-2 break-all sm:break-words dark:text-gray-400 hover:text-yellow-600 dark:hover:text-yellow-100">-->
<!--        <slot/>-->
<!--    </p>-->
<!--    <div class="flex justify-between items-center gap-1 text-left text-gray-500 sm:justify-start sm:flex-row sm:gap-4 md:mb-0 md:text-sm">-->
<!--        &lt;!&ndash; {JSON.stringify(item.readingTime)} &ndash;&gt;-->
<!--        <p>{stringData}</p>-->
<!--        {#if item?.readingTime}-->
<!--            <p class="hidden sm:inline-block">{item?.readingTime}</p>-->
<!--        {/if}-->
<!--        &lt;!&ndash; comment this in if you have multiple categories &ndash;&gt;-->
<!--        <span class="px-4 max-h-6 flex items-center capitalize bg-gray-200 rounded-md dark:bg-gray-700 dark:text-gray-400">-->
<!--				{item?.category || 'note'}-->
<!--			</span>-->
<!--        {#if item?.tags?.length}-->
<!--            <div class="hidden md:block flex-1">-->
<!--                {#each item.tags as tag}-->
<!--					<span class="px-1">-->
<!--						#{tag}-->
<!--					</span>-->
<!--                {/each}-->
<!--            </div>-->
<!--        {/if}-->
<!--    </div>-->
<!--</a>-->