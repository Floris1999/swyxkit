<script>
    import {DEFAULT_OG_IMAGE, MY_TWITTER_HANDLE, SITE_DESCRIPTION, SITE_TITLE, SITE_URL} from '$lib/siteConfig';
    // import hero from '$lib/assets/PXL_20220717_142948860.MP.jpg';
    import hero from '$lib/assets/PXL_20220717_142943888.MP.jpg';
    import Carousel from "../components/Carousel.svelte";

    /** @type {import('./$types').PageData} */
    export let data;
    // technically this is a slighlty different type because doesnt have 'content' but we'll let it slide
    /** @type {import('$lib/types').ContentItem[]} */
</script>

<svelte:head>
    <title>{SITE_TITLE}</title>
    <link rel="canonical" href={SITE_URL}/>
    <link rel="alternate" type="application/rss+xml" href={SITE_URL + '/rss.xml'}/>
    <meta property="og:url" content={SITE_URL}/>
    <meta property="og:type" content="article"/>
    <meta property="og:title" content={SITE_TITLE}/>
    <meta name="Description" content={SITE_DESCRIPTION}/>
    <meta property="og:description" content={SITE_DESCRIPTION}/>
    <meta property="og:image" content={DEFAULT_OG_IMAGE}/>
    <meta name="twitter:card" content="summary"/>
    <meta name="twitter:creator" content={'@' + MY_TWITTER_HANDLE}/>
    <meta name="twitter:title" content={SITE_TITLE}/>
    <meta name="twitter:description" content={SITE_DESCRIPTION}/>
    <meta name="twitter:image" content={DEFAULT_OG_IMAGE}/>
</svelte:head>

<body class="border-x-2 border-black">

<section class="relative flex w-full items-center border-black dark:border-gray-600 border-b-0"
         aria-labelledby="feature-one"
         id="feature-one">
    <div class="relative mx-auto w-full items-center 2xl:max-w-7xl">
        <div class="grid grid-cols-1 divide-y-0 divide-black dark:divide-gray-600 border-black dark:border-gray-600 md:divide-x md:divide-y-0 lg:grid-cols-2 2xl:border-x">
            <div class="relative h-full items-center gap-12 p-8 lg:inline-flex lg:px-20">
                <div class="mx-auto max-w-xl text-left md:text-center lg:text-left">
                    <div>
                        <h2 class="inline-flex items-center text-black dark:text-white"><span
                                class="text-base font-medium tracking-tight">Feature</span> <span
                                class="ml-3 h-3.5 w-px bg-black dark:bg-white"></span> <span class="ml-3 text-sm"
                                                                                             aria-hidden="true">01</span>
                        </h2>
                        <p class="mt-3 text-5xl tracking-tight text-black dark:text-white lg:text-7xl">Floris
                            Wieringa.</p>
                        <p class="mt-4 max-w-xl tracking-tight text-black dark:text-white xl:text-2xl">
                            Full-stack engineer @SINCERIUS based in Amsterdam
                        </p>
                        <ol class="mt-12 grid max-w-xl list-none grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3 lg:gap-12 lg:text-center"
                            role="list">
                            <!--                            <li><h3 class="tracking-tight text-black xl:text-xl">.NET</h3></li>-->
                            <!--                            <li><h3 class="tracking-tight text-black xl:text-xl">60+ Sections</h3></li>-->
                            <!--                            <li><h3 class="tracking-tight text-black xl:text-xl">100+ Components</h3></li>-->
                        </ol>
                    </div>
                    <div class="mt-10 flex flex-col gap-3 sm:flex-row">
                        <a class="inline-flex w-full transform items-center justify-center rounded-xl border-2 border-black bg-white px-6 py-3 text-center text-black shadow-[5px_5px_black] transition duration-200 ease-in-out hover:bg-black hover:text-white hover:shadow-none focus:outline-none lg:w-auto dark:bg-gray-700 dark:hover:bg-gray-900"
                           href="mailto:floris.wieringa@protonmail.com">Contact me<span class="ml-3">→</span></a>
                    </div>
                </div>
            </div>
            <div class="bg-lila-500 block h-100 lg:mt-0 p-4"><img alt="#" class="h-full w-full"
                                                                  src={hero}/></div>
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


<!--<ProjectsCarousal/>-->

<section
        class="relative mx-auto flex w-full items-center border-x border-t-0 border-black 2xl:max-w-7xl dark:border-gray-600"
        aria-labelledby="feature-three" id="feature-three">
    <div class="relative mx-auto w-full items-center">
        <div class="relative h-full items-center gap-12 p-8 lg:p-20">
            <div class="mx-auto max-w-4xl text-center">
                <h2 class="inline-flex items-center text-black"><span
                        class="text-base font-medium tracking-tight dark:text-white">Feature</span>
                    <span class="ml-3 h-3.5 w-px bg-black dark:bg-white"></span> <span
                            class="ml-3 text-sm dark:text-white"
                            aria-hidden="true">02</span></h2>
                <p class="mt-3 text-5xl tracking-tight text-black lg:text-7xl dark:text-white">To put briefly</p>
                <p class="mx-auto mt-4 max-w-xl tracking-tight text-black xl:text-2xl dark:text-white">I love creating
                    all types of software from start to finish and working with new technologies</p>
            </div>
        </div>
    </div>
</section>


<section class="relative flex w-full items-center border-y border-black dark:border-gray-600">
    <div class="relative mx-auto w-full items-center divide-y divide-black border-black 2xl:max-w-7xl 2xl:border-x dark:border-gray-600">
        <div class="grid grid-cols-1 divide-y divide-black md:grid-cols-2 md:divide-x md:divide-y-0">
            <div class="grid grid-cols-1 divide-y-2 divide-black">
                <div class="relative h-full items-center gap-12 bg-orange-600 p-8 py-12 lg:inline-flex lg:px-20 lg:py-32">
                    <div class="mx-auto max-w-xl text-center"><p class="text-5xl tracking-tight text-black">Explore
                        ideas together</p></div>
                </div>

            </div>
            <div class="grid grid-cols-1 divide-y-2 divide-black"
                 style="background-image: linear-gradient(to right, #d9e2e9 1px, transparent 1px),linear-gradient(to bottom, #d9e2e9 1px, transparent 1px); background-size: 40px 40px">
                <div class="bg-lila-500 relative h-full items-center gap-12 p-8 py-12 lg:inline-flex lg:px-20 lg:py-32">
                    <div
                            class="mx-auto max-w-xl text-center"><p
                            class="text-5xl tracking-tight text-black dark:hidden">Bring
                        those
                        ideas to life</p></div>
                </div>

            </div>
        </div>
    </div>
</section>

<section class="relative flex w-full items-center border-b border-black dark:border-gray-600"
         aria-labelledby="feature-four"
         id="feature-four">
    <div class="relative mx-auto w-full items-center 2xl:max-w-7xl">
        <div class="grid grid-cols-1 divide-y divide-black border-black md:grid-cols-2 md:divide-x md:divide-y-0 2xl:border-x dark:border-gray-600">
            <div class="block aspect-square h-full w-full lg:mt-0">
                <Carousel/>
            </div>
            <div class="bg-lila-500 relative h-full items-center gap-12 p-8 lg:inline-flex lg:px-20">
                <div class="max-w-xl text-left">
                    <div>
                        <h2 class="inline-flex items-center text-black dark:text-white"><span
                                class="text-base font-medium tracking-tight">Feature</span> <span
                                class="ml-3 h-3.5 w-px bg-black dark:bg-white"></span> <span class="ml-3 text-sm"
                                                                                             aria-hidden="true">04</span>
                        </h2>
                        <p class="mt-3 text-5xl tracking-tight text-black lg:text-7xl dark:text-white ">In my spare
                            time</p>
                        <p class="mt-4 max-w-xl tracking-tight text-black xl:text-2xl dark:text-white">In addition to
                            programming, I enjoy staying productive during my free time by engaging in various
                            activities:</p>
                    </div>
                    <div class="mt-6">
                        <ul class="flex flex-col tracking-tight text-black xl:text-xl dark:text-white list-disc">
                            <li class=" items-center gap-3">
                                Surfing &#127940;
                            </li>
                            <li class=" items-center gap-3">
                                Making music &#x1F3B8;
                            </li>
                            <li class=" items-center gap-3">
                                Chess &#x1F451;
                            </li>
                            <li class=" items-center gap-3">
                                Cycling &#x1F6B4;
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

</body>