<script>
    import {DEFAULT_OG_IMAGE, MY_TWITTER_HANDLE, SITE_DESCRIPTION, SITE_TITLE, SITE_URL} from '$lib/siteConfig';
    // import hero from '$lib/assets/PXL_20220717_142948860.MP.jpg';
    import hero from '$lib/assets/PXL_20220717_142943888.MP.jpg';
    import Carousel from "../components/Carousel.svelte";

    /** @type {import('./$types').PageData} */
    export let data;
    // technically this is a slighlty different type because doesnt have 'content' but we'll let it slide
    /** @type {import('$lib/types').ContentItem[]} */
    $: items = data.items;
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

<section class="relative flex w-full items-center border-black dark:border-gray-600 border-b-0" aria-labelledby="feature-one"
         id="feature-one">
    <div class="relative mx-auto w-full items-center 2xl:max-w-7xl">
        <div class="grid grid-cols-1 divide-y-0 divide-black dark:divide-gray-600 border-black dark:border-gray-600 md:divide-x md:divide-y-0 lg:grid-cols-2 2xl:border-x">
            <div class="relative h-full items-center gap-12 p-8 lg:inline-flex lg:px-20">
                <div class="mx-auto max-w-xl text-left md:text-center lg:text-left">
                    <div>
                        <h2 class="inline-flex items-center text-black dark:text-white"><span
                                class="text-base font-medium tracking-tight">Feature</span> <span
                                class="ml-3 h-3.5 w-px bg-black dark:bg-white"></span> <span class="ml-3 text-sm" aria-hidden="true">01</span>
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

<section class="relative mx-auto flex w-full items-center border-x border-t-0 border-black 2xl:max-w-7xl dark:border-gray-600"
         aria-labelledby="feature-three" id="feature-three">
    <div class="relative mx-auto w-full items-center">
        <div class="relative h-full items-center gap-12 p-8 lg:p-20">
            <div class="mx-auto max-w-4xl text-center">
                <h2 class="inline-flex items-center text-black"><span class="text-base font-medium tracking-tight dark:text-white">Feature</span>
                    <span class="ml-3 h-3.5 w-px bg-black dark:bg-white"></span> <span class="ml-3 text-sm dark:text-white"
                                                                         aria-hidden="true">02</span></h2>
                <p class="mt-3 text-5xl tracking-tight text-black lg:text-7xl dark:text-white">To put briefly</p>
                <p class="mx-auto mt-4 max-w-xl tracking-tight text-black xl:text-2xl dark:text-white">I love creating all types of software from start to finish and working with new technologies</p>
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
                            class="mx-auto max-w-xl text-center"><p class="text-5xl tracking-tight text-black dark:hidden">Bring
                        those
                        ideas to life</p></div>
                </div>

            </div>
        </div>
    </div>
</section>

<section class="relative flex w-full items-center border-b border-black dark:border-gray-600" aria-labelledby="feature-four"
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
                                class="ml-3 h-3.5 w-px bg-black dark:bg-white"></span> <span class="ml-3 text-sm" aria-hidden="true">04</span>
                        </h2>
                        <p class="mt-3 text-5xl tracking-tight text-black lg:text-7xl dark:text-white ">In my spare time</p>
                        <p class="mt-4 max-w-xl tracking-tight text-black xl:text-2xl dark:text-white">In addition to programming, I enjoy staying productive during my free time by engaging in various activities:</p>
                    </div>
                    <div class="mt-6">
                        <ul class="flex flex-col tracking-tight text-black xl:text-xl dark:text-white" role="list">
                            <li class="inline-flex items-center gap-3">
                                <svg fill="none" viewBox="0 0 27 28" xmlns="http://www.w3.org/2000/svg" height="18"
                                     width="17">
                                    <path d="M15.0001 2.24991C15.0001 1.42153 14.3285 0.75 13.5002 0.75V0.75C12.6718 0.75 12.0002 1.42153 12.0002 2.24991V3.6505C12.0002 6.23455 8.87605 7.52867 7.04882 5.70151L5.85321 4.50596C5.27398 3.92675 4.33489 3.92676 3.75567 4.50598V4.50598C3.17645 5.0852 3.17644 6.0243 3.75564 6.60353L4.95104 7.79898C6.77802 9.62604 5.48402 12.7499 2.90022 12.7499H1.49991C0.671531 12.7499 0 13.4215 0 14.2498V14.2498C0 15.0782 0.671533 15.7498 1.49991 15.7498H2.89968C5.48298 15.7498 6.77673 18.8731 4.9501 20.6998L3.75061 21.8993C3.17107 22.4789 3.17108 23.4185 3.75063 23.9981V23.9981C4.3302 24.5777 5.26987 24.5777 5.84944 23.9981L7.04889 22.7986C8.87606 20.9715 12.0002 22.2655 12.0002 24.8496V26.2501C12.0002 27.0785 12.6718 27.75 13.5002 27.75V27.75C14.3285 27.75 15.0001 27.0785 15.0001 26.2501V24.8498C15.0001 22.2661 18.124 20.9721 19.951 22.7991L21.1514 23.9995C21.7307 24.5788 22.6699 24.5788 23.2492 23.9995V23.9995C23.8285 23.4202 23.8285 22.481 23.2492 21.9017L22.0486 20.7011C20.2215 18.8739 21.5155 15.7498 24.0996 15.7498H25.5001C26.3285 15.7498 27 15.0782 27 14.2498V14.2498C27 13.4215 26.3285 12.7499 25.5001 12.7499H24.0997C21.5157 12.7499 20.2217 9.62585 22.0488 7.79873L23.2434 6.60414C23.823 6.02457 23.823 5.08492 23.2434 4.50535V4.50535C22.6638 3.92579 21.7242 3.92579 21.1446 4.50536L19.95 5.69995C18.1234 7.5266 15.0001 6.23289 15.0001 3.64961V2.24991Z"
                                          fill="black" clip-rule="evenodd" fill-rule="evenodd"></path>
                                </svg>
                                Surfing &#127940;
                            </li>
                            <li class="inline-flex items-center gap-3">
                                <svg fill="none" viewBox="0 0 27 28" xmlns="http://www.w3.org/2000/svg" height="18"
                                     width="17">
                                    <path d="M15.0001 2.24991C15.0001 1.42153 14.3285 0.75 13.5002 0.75V0.75C12.6718 0.75 12.0002 1.42153 12.0002 2.24991V3.6505C12.0002 6.23455 8.87605 7.52867 7.04882 5.70151L5.85321 4.50596C5.27398 3.92675 4.33489 3.92676 3.75567 4.50598V4.50598C3.17645 5.0852 3.17644 6.0243 3.75564 6.60353L4.95104 7.79898C6.77802 9.62604 5.48402 12.7499 2.90022 12.7499H1.49991C0.671531 12.7499 0 13.4215 0 14.2498V14.2498C0 15.0782 0.671533 15.7498 1.49991 15.7498H2.89968C5.48298 15.7498 6.77673 18.8731 4.9501 20.6998L3.75061 21.8993C3.17107 22.4789 3.17108 23.4185 3.75063 23.9981V23.9981C4.3302 24.5777 5.26987 24.5777 5.84944 23.9981L7.04889 22.7986C8.87606 20.9715 12.0002 22.2655 12.0002 24.8496V26.2501C12.0002 27.0785 12.6718 27.75 13.5002 27.75V27.75C14.3285 27.75 15.0001 27.0785 15.0001 26.2501V24.8498C15.0001 22.2661 18.124 20.9721 19.951 22.7991L21.1514 23.9995C21.7307 24.5788 22.6699 24.5788 23.2492 23.9995V23.9995C23.8285 23.4202 23.8285 22.481 23.2492 21.9017L22.0486 20.7011C20.2215 18.8739 21.5155 15.7498 24.0996 15.7498H25.5001C26.3285 15.7498 27 15.0782 27 14.2498V14.2498C27 13.4215 26.3285 12.7499 25.5001 12.7499H24.0997C21.5157 12.7499 20.2217 9.62585 22.0488 7.79873L23.2434 6.60414C23.823 6.02457 23.823 5.08492 23.2434 4.50535V4.50535C22.6638 3.92579 21.7242 3.92579 21.1446 4.50536L19.95 5.69995C18.1234 7.5266 15.0001 6.23289 15.0001 3.64961V2.24991Z"
                                          fill="black" clip-rule="evenodd" fill-rule="evenodd"></path>
                                </svg>
                                Making music &#x1F3B8;
                            </li>
                            <li class="inline-flex items-center gap-3">
                                <svg fill="none" viewBox="0 0 27 28" xmlns="http://www.w3.org/2000/svg" height="18"
                                     width="17">
                                    <path d="M15.0001 2.24991C15.0001 1.42153 14.3285 0.75 13.5002 0.75V0.75C12.6718 0.75 12.0002 1.42153 12.0002 2.24991V3.6505C12.0002 6.23455 8.87605 7.52867 7.04882 5.70151L5.85321 4.50596C5.27398 3.92675 4.33489 3.92676 3.75567 4.50598V4.50598C3.17645 5.0852 3.17644 6.0243 3.75564 6.60353L4.95104 7.79898C6.77802 9.62604 5.48402 12.7499 2.90022 12.7499H1.49991C0.671531 12.7499 0 13.4215 0 14.2498V14.2498C0 15.0782 0.671533 15.7498 1.49991 15.7498H2.89968C5.48298 15.7498 6.77673 18.8731 4.9501 20.6998L3.75061 21.8993C3.17107 22.4789 3.17108 23.4185 3.75063 23.9981V23.9981C4.3302 24.5777 5.26987 24.5777 5.84944 23.9981L7.04889 22.7986C8.87606 20.9715 12.0002 22.2655 12.0002 24.8496V26.2501C12.0002 27.0785 12.6718 27.75 13.5002 27.75V27.75C14.3285 27.75 15.0001 27.0785 15.0001 26.2501V24.8498C15.0001 22.2661 18.124 20.9721 19.951 22.7991L21.1514 23.9995C21.7307 24.5788 22.6699 24.5788 23.2492 23.9995V23.9995C23.8285 23.4202 23.8285 22.481 23.2492 21.9017L22.0486 20.7011C20.2215 18.8739 21.5155 15.7498 24.0996 15.7498H25.5001C26.3285 15.7498 27 15.0782 27 14.2498V14.2498C27 13.4215 26.3285 12.7499 25.5001 12.7499H24.0997C21.5157 12.7499 20.2217 9.62585 22.0488 7.79873L23.2434 6.60414C23.823 6.02457 23.823 5.08492 23.2434 4.50535V4.50535C22.6638 3.92579 21.7242 3.92579 21.1446 4.50536L19.95 5.69995C18.1234 7.5266 15.0001 6.23289 15.0001 3.64961V2.24991Z"
                                          fill="black" clip-rule="evenodd" fill-rule="evenodd"></path>
                                </svg>
                                Chess &#x1F451;
                            </li>
                            <li class="inline-flex items-center gap-3">
                                <svg fill="none" viewBox="0 0 27 28" xmlns="http://www.w3.org/2000/svg" height="18"
                                     width="17">
                                    <path d="M15.0001 2.24991C15.0001 1.42153 14.3285 0.75 13.5002 0.75V0.75C12.6718 0.75 12.0002 1.42153 12.0002 2.24991V3.6505C12.0002 6.23455 8.87605 7.52867 7.04882 5.70151L5.85321 4.50596C5.27398 3.92675 4.33489 3.92676 3.75567 4.50598V4.50598C3.17645 5.0852 3.17644 6.0243 3.75564 6.60353L4.95104 7.79898C6.77802 9.62604 5.48402 12.7499 2.90022 12.7499H1.49991C0.671531 12.7499 0 13.4215 0 14.2498V14.2498C0 15.0782 0.671533 15.7498 1.49991 15.7498H2.89968C5.48298 15.7498 6.77673 18.8731 4.9501 20.6998L3.75061 21.8993C3.17107 22.4789 3.17108 23.4185 3.75063 23.9981V23.9981C4.3302 24.5777 5.26987 24.5777 5.84944 23.9981L7.04889 22.7986C8.87606 20.9715 12.0002 22.2655 12.0002 24.8496V26.2501C12.0002 27.0785 12.6718 27.75 13.5002 27.75V27.75C14.3285 27.75 15.0001 27.0785 15.0001 26.2501V24.8498C15.0001 22.2661 18.124 20.9721 19.951 22.7991L21.1514 23.9995C21.7307 24.5788 22.6699 24.5788 23.2492 23.9995V23.9995C23.8285 23.4202 23.8285 22.481 23.2492 21.9017L22.0486 20.7011C20.2215 18.8739 21.5155 15.7498 24.0996 15.7498H25.5001C26.3285 15.7498 27 15.0782 27 14.2498V14.2498C27 13.4215 26.3285 12.7499 25.5001 12.7499H24.0997C21.5157 12.7499 20.2217 9.62585 22.0488 7.79873L23.2434 6.60414C23.823 6.02457 23.823 5.08492 23.2434 4.50535V4.50535C22.6638 3.92579 21.7242 3.92579 21.1446 4.50536L19.95 5.69995C18.1234 7.5266 15.0001 6.23289 15.0001 3.64961V2.24991Z"
                                          fill="black" clip-rule="evenodd" fill-rule="evenodd"></path>
                                </svg>
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