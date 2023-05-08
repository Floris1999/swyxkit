<script>
    import ExperienceMenu from "../../components/ExperienceMenu.svelte";
    import leiden from '$lib/assets/leiden.jpg';
    import nrcLight from "$lib/assets/nrc-light.png";

    let experience = [
        {
            title: "Full Stack SINCERIUS",
            startedAt: "Sept 1 2023",
            endedAt: "Current",
            href: "#section-1"
        },
        {
            title: "Front-end internship SINCERIUS",
            startedAt: "2023-04-22T00:00:00.000Z",
            endedAt: "2023-04-22T00:00:00.000Z",
            href: "#section-2"
        },
        {
            title: "Computer BSc Hogeschool Leiden",
            startedAt: "2023-04-22T00:00:00.000Z",
            endedAt: "2023-04-22T00:00:00.000Z",
            href: "#section-3"
        },
        {
            title: "Android Developer Pinch / Internship",
            startedAt: "2023-04-22T00:00:00.000Z",
            endedAt: "2023-04-22T00:00:00.000Z",
            href: "#section-4"
        },
    ]

    let projects = [
        {
            title: "Title",
            startedAt: "2023-04-22T00:00:00.000Z",
            endedAt: "2023-04-22T00:00:00.000Z",
            href: ""
        },

        {
            title: "Title",
            startedAt: "2023-04-22T00:00:00.000Z",
            endedAt: "2023-04-22T00:00:00.000Z",
            href: ""
        },
    ]
</script>

<svelte:head>

</svelte:head>

<div class="mx-auto divide-black dark:divide-gray-600 border-b border-black lg:flex lg:divide-x 2xl:max-w-7xl 2xl:border-x dark:border-gray-600">
    <ExperienceMenu experience={experience} title="My Experience"/>

    <div class="p-8 lg:w-1/2 lg:p-20">
        <div class="flex-shrink-0">
            <div>
                <div>
                    <div class="relative mb-24 pl-[38px] font-polysans lg:pl-50">
                        <div><h2 class="mb-8 text-16 leading-120 tracking-2 text-black dark:text-white">My work
                            experience</h2>
                            <div class="absolute top-4 left-[9px] h-12 w-12 rounded-full md:left-6 lg:left-16 bg-gray-bd dark:bg-[#313131]"></div>
                        </div>
                        <p class="mb-4 text-11 uppercase leading-140 tracking-15"><span
                                class="block text-gray-63 dark:text-gray-94">Feed refreshed at 17 Apr 2023</span>
                        </p></div>
                    <div class="mb-6 ml-[38px] w-60 border-t border-gray-bd dark:border-gray-4a lg:mb-0 lg:ml-50"></div>
                </div>

                <ul class="grid list-none grid-cols-1 gap-12 lg:gap-24" role="list">
                    <li class="shadow-large border-2 border-black bg-green-500 p-8">
                        <div class="hover:prose-a:decoration-mint hover:prose-a:text-red-500 prose prose-3xl prose-a:decoration-mercury-400 prose-a:font-semibold prose-a:text-black text-black">
                            <h2>Full Stack SINCERIUS</h2>
                            <p>28 May, 2023</p>
                            <a class="inline-flex items-center"
                               href="https://sincerius.nl/en/services/business-intelligence-solutions/">SINCERIUS BI</a>

                            <p>
                                I played a key role as the head front-end developer in React during my internship on a
                                project that involved fetching and analyzing data from multiple sources of a company,
                                with 50.000 monthly logins and managing well over 1 billion of customer assets. </p>

                            <p>Later I moved to full stack to also help with fetching company data and working on the
                                .NET backend</p>
                        </div>
                    </li>
                    <li class="shadow-large border-2 border-black p-8">
                        <div class="hover:prose-a:decoration-mint hover:prose-a:text-red-500 prose prose-3xl prose-a:decoration-mercury-400 prose-a:font-semibold prose-a:text-black pt-12 text-black">
                            <h2>Hogeschool Leiden</h2>
                            <p>16 March, 2023</p>
                            <a class="inline-flex items-center" href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Watch
                                update video</a>
                            <p>In January 2, I completed my Bachelor of Science in Computer Science at Hogeschool
                                Leiden, with a specialization in user design and interaction.</p>
                            <img alt="#" class=" border border-black"
                                 src={leiden}/>
                        </div>

                    </li>
                    <li class="shadow-large border-2 border-black bg-red-500 p-8">
                        <div class="hover:prose-a:decoration-mint hover:prose-a:text-red-500 prose prose-3xl prose-a:decoration-mercury-400 prose-a:font-semibold prose-a:text-black pt-12 text-black">
                            <h2>Android Developer PINCH</h2>
                            <p>8 January, 2023</p>
                            <h3>NRC</h3>
                            <p>Here I worked on the app of the third biggest news paper android app of the Netherlands with <a href="https://www.nrc.nl/nieuws/2021/03/19/nrc-bereikt-grens-van-300000-abonnees-a4036389">300.000</a> subscribers </p>
                            <img alt="#" class="border border-black h-100"
                                 src={nrcLight}/>
                        </div>
                    </li>
<!--                    <li class="shadow-large border-2 border-black bg-yellow-500 p-8">-->
<!--                        <div class="hover:prose-a:decoration-mint hover:prose-a:text-red-500 prose prose-3xl prose-a:decoration-mercury-400 prose-a:font-semibold prose-a:text-black text-black">-->
<!--                            <h2>Version 4.4</h2>-->
<!--                            <p>28 May, 2023</p>-->
<!--                            <a class="inline-flex items-center" href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Watch-->
<!--                                update video</a>-->
<!--                            <ul>-->
<!--                                <li>Introducing Capture History - easily access and restore recent captures</li>-->
<!--                                <li>Added Auto-Scroll option to Scrolling Capture</li>-->
<!--                                <li>Added option to copy/paste objects in Annotate</li>-->
<!--                                <li>New OCR language support in macOS Ventura - Korean, Japanese, Russian, Ukrainian-->
<!--                                </li>-->
<!--                                <li>Improved Annotate compatiblity with some trackpads</li>-->
<!--                                <li>Disabled cursor when capturing full screen with All-In-One</li>-->
<!--                                <li>Fixed bug causing misaligned scrolling captures</li>-->
<!--                                <li>Fixed bug with auto-expanding canvas</li>-->
<!--                                <li>Fixed bug with freezing screen after starting screen recordings multiple ps</li>-->
<!--                                <li>Fixed bug with showing recording controls on specific display setups</li>-->
<!--                                <li>Fixed bug with using "Expire After" option in upload dialog</li>-->
<!--                                <li>Minor changes in URL Scheme API</li>-->
<!--                                <li>Small bug fixes and UX improvements</li>-->
<!--                            </ul>-->
<!--                        </div>-->
<!--                    </li>-->
                </ul>
            </div>
        </div>
    </div>
</div>

<div class="mx-auto divide-black dark:divide-gray-600 border-b 2xl:border-x border-black lg:flex lg:divide-x 2xl:max-w-7xl dark:border-gray-600">
    <div class="p-8 lg:w-1/2 lg:p-20">
        <div class="flex-shrink-0">
            <div>
                <div>
                    <div class="duet--recirculation--storystream-header relative mb-24 pl-[38px] font-polysans lg:pl-50">
                        <div><h2 class="mb-8 text-16 leading-120 tracking-2 text-black dark:text-white">My work
                            experience</h2>
                            <div class="duet--recirculation--storystream-header-beacon absolute top-4 left-[9px] h-12 w-12 rounded-full md:left-6 lg:left-16 bg-gray-bd dark:bg-[#313131]"></div>
                        </div>
                        <p class="mb-4 text-11 uppercase leading-140 tracking-15"><span
                                class="block text-gray-63 dark:text-gray-94">Feed refreshed at 17 Apr 2023</span>
                        </p></div>
                    <div class="mb-6 ml-[38px] w-60 border-t border-gray-bd dark:border-gray-4a lg:mb-0 lg:ml-50"></div>
                </div>

                <ul class="grid list-none grid-cols-1 gap-12 lg:gap-24" role="list">
                    <li class="shadow-large border-2 border-black bg-green-500 p-8">
                        <div class="hover:prose-a:decoration-mint hover:prose-a:text-red-500 prose prose-3xl prose-a:decoration-mercury-400 prose-a:font-semibold prose-a:text-black text-black">
                            <h2>Version 4.4</h2>
                            <p>28 May, 2023</p>
                            <a class="inline-flex items-center" href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Watch
                                update video</a>
                            <ul>
                                <li>Introducing Capture History - easily access and restore recent captures</li>
                                <li>Added Auto-Scroll option to Scrolling Capture</li>
                                <li>Added option to copy/paste objects in Annotate</li>
                                <li>New OCR language support in macOS Ventura - Korean, Japanese, Russian, Ukrainian
                                </li>
                                <li>Improved Annotate compatiblity with some trackpads</li>
                                <li>Disabled cursor when capturing full screen with All-In-One</li>
                                <li>Fixed bug causing misaligned scrolling captures</li>
                                <li>Fixed bug with auto-expanding canvas</li>
                                <li>Fixed bug with freezing screen after starting screen recordings multiple ps</li>
                                <li>Fixed bug with showing recording controls on specific display setups</li>
                                <li>Fixed bug with using "Expire After" option in upload dialog</li>
                                <li>Minor changes in URL Scheme API</li>
                                <li>Small bug fixes and UX improvements</li>
                            </ul>
                        </div>
                    </li>
                    <li class="shadow-large border-2 border-black p-8">
                        <div class="hover:prose-a:decoration-mint hover:prose-a:text-red-500 prose prose-3xl prose-a:decoration-mercury-400 prose-a:font-semibold prose-a:text-black pt-12 text-black">
                            <h2>Version 3.11</h2>
                            <p>16 March, 2023</p>
                            <a class="inline-flex items-center" href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Watch
                                update video</a>
                            <ul>
                                <li>Added new setting that allows to change behavior of "Capture Area &amp;..."
                                    shortcuts
                                </li>
                                <li>Improved combining images in Annotate after cropping</li>
                                <li>Fixed bug with using Command+/Command- shortcuts on some keyboard layouts</li>
                                <li>Minor bug fixes and improvements</li>
                            </ul>
                        </div>
                    </li>
                    <li class="shadow-large border-2 border-black bg-red-500 p-8">
                        <div class="hover:prose-a:decoration-mint hover:prose-a:text-red-500 prose prose-3xl prose-a:decoration-mercury-400 prose-a:font-semibold prose-a:text-black pt-12 text-black">
                            <h2>Version 2.3.3</h2>
                            <p>8 January, 2023</p>
                            <ul>
                                <li>Added new setting that allows to change behavior of "Capture Area &amp;..."
                                    shortcuts
                                </li>
                                <li>Improved combining images in Annotate after cropping</li>
                            </ul>
                        </div>
                    </li>
                    <li class="shadow-large border-2 border-black bg-yellow-500 p-8">
                        <div class="hover:prose-a:decoration-mint hover:prose-a:text-red-500 prose prose-3xl prose-a:decoration-mercury-400 prose-a:font-semibold prose-a:text-black text-black">
                            <h2>Version 4.4</h2>
                            <p>28 May, 2023</p>
                            <a class="inline-flex items-center" href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">Watch
                                update video</a>
                            <ul>
                                <li>Introducing Capture History - easily access and restore recent captures</li>
                                <li>Added Auto-Scroll option to Scrolling Capture</li>
                                <li>Added option to copy/paste objects in Annotate</li>
                                <li>New OCR language support in macOS Ventura - Korean, Japanese, Russian, Ukrainian
                                </li>
                                <li>Improved Annotate compatiblity with some trackpads</li>
                                <li>Disabled cursor when capturing full screen with All-In-One</li>
                                <li>Fixed bug causing misaligned scrolling captures</li>
                                <li>Fixed bug with auto-expanding canvas</li>
                                <li>Fixed bug with freezing screen after starting screen recordings multiple ps</li>
                                <li>Fixed bug with showing recording controls on specific display setups</li>
                                <li>Fixed bug with using "Expire After" option in upload dialog</li>
                                <li>Minor changes in URL Scheme API</li>
                                <li>Small bug fixes and UX improvements</li>
                            </ul>
                        </div>
                    </li>
                </ul>
            </div>
        </div>
    </div>


    <ExperienceMenu experience={projects} title="My Projects" style="background-color: rgba(255,61,0,.9)"/>

    <!--    <div class="p-8 lg:w-1/2 lg:p-20">-->
    <!--        <div class="lg:sticker top-40 py-8 lg:sticky lg:py-20">-->
    <!--            <div style="background-color: rgba(255,61,0,.9)" class="duet&#45;&#45;recirculation&#45;&#45;list-breaker-compact ml:m-auto relative mt-80 ml-[65px] min-h-[475px] w-mobile-breaker  rounded-[4px] p-20 sm:w-tablet-breaker md:mb-40  lg:sticky lg:top-40 lg:mt-0  lg:ml-0 lg:min-h-[600px] lg:w-desktop-breaker lg:overflow-hidden lg:rounded-[20px] text-white">-->
    <!--                <h2 class="absolute top-[-25px] left-[-80px] -z-10 flex rotate-180 font-manuka text-[110px] font-ultra leading-100 tracking-1 text-gray-13 dark:text-white lg:hidden"-->
    <!--                    style="writing-mode: vertical-rl; text-orientation: sideways;">My experience</h2>-->
    <!--                <div class="text-9 relative z-10 mb-20 flex justify-between font-polysans  text-10 uppercase tracking-15">-->
    <!--                    <span class="font-medium">My experience</span></div>-->
    <!--                <div class="absolute right-0 bottom-[-10px] mr-[-25px] hidden h-full rotate-180 font-manuka text-[190px] font-ultra  leading-100 lg:flex text-blurple-39"-->
    <!--                     style="writing-mode: vertical-rl; text-orientation: sideways;">My experience-->
    <!--                </div>-->
    <!--                <ol class="styled-counter w-full lg:mt-20 lg:w-[320px] styled-counter-compact">-->
    <!--                    {#each experience as item, i}-->
    <!--                        <li class="mb-20 border-b pb-20 text-franklin last:mb-0 last:border-0 last:pb-0 lg:last:mb-20 border-b-franklin">-->
    <!--                            <a class="text-white hover:text-franklin mb-4 font-polysans text-18 font-medium leading-110 tracking-1"-->
    <!--                               on:click|preventDefault={scrollIntoView}-->
    <!--                               href={item.href}>-->
    <!--                                {item.title}-->
    <!--                            </a>-->
    <!--                            <p class="duet&#45;&#45;recirculation&#45;&#45;breaker-byline font-polysans text-11 uppercase leading-140 tracking-15">-->
    <!--                                <span class="mr-8 text-gray-ef">{item.startedAt}</span><span-->
    <!--                                    class="mr-8 font-light text-gray-ef">{item.endedAt}</span></p>-->
    <!--                        </li>-->
    <!--                    {/each}-->
    <!--                </ol>-->
    <!--            </div>-->
    <!--        </div>-->
    <!--    </div>-->

</div>


<style>
    .absolute {
        position: absolute
    }

    .relative {
        position: relative
    }

    .right-0 {
        right: 0
    }

    .top-\[-25px\] {
        top: -25px
    }

    .left-\[-80px\] {
        left: -80px
    }

    .bottom-\[-10px\] {
        bottom: -10px
    }

    .top-4 {
        top: 4px
    }

    .left-\[9px\] {
        left: 9px
    }

    .z-10 {
        z-index: 10
    }

    .-z-10 {
        z-index: -10
    }

    .mx-auto {
        margin-left: auto;
        margin-right: auto
    }

    .mb-4 {
        margin-bottom: 4px
    }

    .mb-8 {
        margin-bottom: 8px
    }

    .mb-24 {
        margin-bottom: 24px
    }

    .mb-20 {
        margin-bottom: 20px
    }

    .mr-8 {
        margin-right: 8px
    }

    .mb-6 {
        margin-bottom: 6px
    }

    .mt-80 {
        margin-top: 80px
    }

    .ml-\[65px\] {
        margin-left: 65px
    }

    .mr-\[-25px\] {
        margin-right: -25px
    }

    .ml-\[38px\] {
        margin-left: 38px
    }

    .block {
        display: block
    }

    .flex {
        display: flex
    }

    .hidden {
        display: none
    }

    .h-full {
        height: 100%
    }

    .h-12 {
        height: 12px
    }

    .min-h-\[475px\] {
        min-height: 475px
    }

    .w-full {
        width: 100%
    }

    .w-12 {
        width: 12px
    }

    .w-mobile-breaker {
        width: 300px
    }

    .w-60 {
        width: 60px
    }

    .rotate-180 {
        --tw-rotate: 180deg
    }

    @keyframes pulse {
        50% {
            opacity: .5
        }
    }

    @keyframes stream-entry-change-color {
        0% {
            background-color: #fff
        }
        25% {
            background-color: rgba(60, 255, 208, .05)
        }
        50% {
            background-color: rgba(60, 255, 208, .1)
        }
        26% {
            background-color: rgba(60, 255, 208, .05)
        }
        to {
            background-color: #fff
        }
    }

    @keyframes spin {
        to {
            transform: rotate(1turn)
        }
    }

    @keyframes scale {
        0% {
            transform: scale(1)
        }
        50% {
            transform: scale(0)
        }
        to {
            transform: scale(1)
        }
    }

    .items-center {
        align-items: center
    }

    .justify-between {
        justify-content: space-between
    }

    .space-y-20 > :not([hidden]) ~ :not([hidden]) {
        --tw-space-y-reverse: 0;
        margin-top: calc(20px * calc(1 - var(--tw-space-y-reverse)));
        margin-bottom: calc(20px * var(--tw-space-y-reverse))
    }

    .space-x-\[3px\] > :not([hidden]) ~ :not([hidden]) {
        --tw-space-x-reverse: 0;
        margin-right: calc(3px * var(--tw-space-x-reverse));
        margin-left: calc(3px * calc(1 - var(--tw-space-x-reverse)))
    }

    .divide-y > :not([hidden]) ~ :not([hidden]) {
        --tw-divide-y-reverse: 0;
        border-top-width: calc(1px * calc(1 - var(--tw-divide-y-reverse)));
        border-bottom-width: calc(1px * var(--tw-divide-y-reverse))
    }

    .divide-gray-cc > :not([hidden]) ~ :not([hidden]) {
        --tw-divide-opacity: 1;
        border-color: rgb(204 204 204/var(--tw-divide-opacity))
    }

    .rounded-full {
        border-radius: 9999px
    }

    .rounded-\[4px\] {
        border-radius: 4px
    }

    .border-b {
        border-bottom-width: 1px
    }

    .border-gray-bd {
        --tw-border-opacity: 1;
        border-color: rgb(189 189 189/var(--tw-border-opacity))
    }

    .border-b-franklin {
        --tw-border-opacity: 1;
        border-bottom-color: rgb(60 255 208/var(--tw-border-opacity))
    }

    .bg-gray-bd {
        --tw-bg-opacity: 1;
        background-color: rgb(189 189 189/var(--tw-bg-opacity))
    }

    .p-20 {
        padding: 20px
    }

    .pt-12 {
        padding-top: 12px
    }

    .pb-20 {
        padding-bottom: 20px
    }

    .pl-\[38px\] {
        padding-left: 38px
    }

    .font-polysans {
        font-family: var(--font-polysans)
    }

    .font-manuka {
        font-family: var(--font-manuka)
    }

    .text-18 {
        font-size: 18px
    }

    .text-16 {
        font-size: 16px
    }

    .text-11 {
        font-size: 11px
    }

    .text-10 {
        font-size: 10px
    }

    .text-\[110px\] {
        font-size: 110px
    }

    .text-\[190px\] {
        font-size: 190px
    }

    .font-light {
        font-weight: 300
    }

    .font-medium {
        font-weight: 500
    }

    .font-ultra {
        font-weight: 1000
    }

    .uppercase {
        text-transform: uppercase
    }

    .leading-140 {
        line-height: 1.4
    }

    .leading-120 {
        line-height: 1.2
    }

    .leading-100 {
        line-height: 1
    }

    .leading-110 {
        line-height: 1.1
    }

    .tracking-15 {
        letter-spacing: .15em
    }

    .tracking-1 {
        letter-spacing: .01em
    }

    .tracking-2 {
        letter-spacing: .02em
    }

    .text-black {
        --tw-text-opacity: 1;
        color: rgb(0 0 0/var(--tw-text-opacity))
    }

    .text-white {
        --tw-text-opacity: 1;
        color: rgb(255 255 255/var(--tw-text-opacity))
    }

    .text-gray-13 {
        --tw-text-opacity: 1;
        color: rgb(19 19 19/var(--tw-text-opacity))
    }

    .text-franklin {
        --tw-text-opacity: 1;
        color: rgb(60 255 208/var(--tw-text-opacity))
    }

    .text-gray-63 {
        --tw-text-opacity: 1;
        color: rgb(99 99 99/var(--tw-text-opacity))
    }

    .text-gray-ef {
        --tw-text-opacity: 1;
        color: rgb(239 239 239/var(--tw-text-opacity))
    }

    .text-blurple-39 {
        --tw-text-opacity: 1;
        color: rgb(57 4 171/var(--tw-text-opacity))
    }

    .m-ad iframe {
        margin: 0 auto;
        max-width: 100%
    }

    .m-ad__hub_sponsorship iframe {
        margin-right: unset;
        margin-left: auto
    }

    .m-ad__native-mobile__image img {
        max-height: 75px;
        max-width: 75px;
        border-radius: 2px
    }

    .m-ad__native-mobile__byline img {
        max-height: 120px;
        max-width: 24px;
        margin-left: 8px
    }

    .dfp_ad--held-area > div {
        z-index: 2;
        position: relative
    }

    @media only screen and (max-width: 767px) {
    }

    @media (min-width: 768px) {
    }

    @media (min-width: 1181px) {
    }

    .duet--article--more-stories + div[data-concert-ads-name=athena_article_mobile] {
        padding-left: 20px;
        padding-right: 20px
    }

    @media (min-width: 1181px) {
    }

    @media (min-width: 1181px) {
    }

    .tiktok-embed > section {
        color: #131313
    }

    .styled-counter {
        counter-reset: counter;
        list-style: none
    }

    .styled-counter li {
        counter-increment: counter;
        position: relative;
        padding-left: 28px
    }

    .styled-counter li:before {
        content: counter(counter);
        position: absolute;
        left: -4px;
        width: 22px;
        height: 22px;
        border-radius: 50%;
        text-align: center;
        font-family: var(--font-polysans);
        font-size: 14px
    }

    .styled-counter-playlist li:before {
        content: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='7' height='8' viewBox='0 0 7 8' fill='none'%3E%3Cpath d='M7 4L0 8L3.53316e-07 0L7 4Z' fill='%23309875'/%3E%3C/svg%3E");
        text-align: unset;
        padding-left: 9px;
        top: -1px;
        --tw-bg-opacity: 1;
        background-color: rgb(19 19 19/var(--tw-bg-opacity));
        font-size: 13px
    }

    .styled-counter-compact li:before {
        background-color: rgba(0, 0, 0, .5)
    }

    .styled-counter-standard li:before {
        background-color: transparent;
        font-size: 16px;
        font-weight: 700
    }

    .duet--article--dangerously-set-cms-markup a[href*="/review-score-update-processes"] {
        display: none
    }

    .marker\:font-polysans-mono ::marker {
        font-family: var(--font-polysans-mono)
    }

    .marker\:text-18 ::marker {
        font-size: 18px
    }

    .marker\:font-light ::marker {
        font-weight: 300
    }

    .marker\:text-blurple\/100 ::marker {
        color: #5200ff
    }

    .marker\:text-blurple ::marker {
        color: #5200ff
    }

    .marker\:text-franklin ::marker {
        color: #3cffd0
    }

    .selection\:bg-franklin-20 ::-moz-selection {
        --tw-bg-opacity: 1;
        background-color: rgb(216 255 246/var(--tw-bg-opacity))
    }

    .selection\:bg-franklin-20 ::selection {
        --tw-bg-opacity: 1;
        background-color: rgb(216 255 246/var(--tw-bg-opacity))
    }

    .first-letter\:selection\:bg-franklin-20 :first-letter::-moz-selection {
        --tw-bg-opacity: 1;
        background-color: rgb(216 255 246/var(--tw-bg-opacity))
    }

    .first-letter\:selection\:bg-franklin-20 :first-letter::selection {
        --tw-bg-opacity: 1;
        background-color: rgb(216 255 246/var(--tw-bg-opacity))
    }

    .last\:mb-0:last-child {
        margin-bottom: 0
    }

    .last\:border-0:last-child {
        border-width: 0
    }

    .last\:pb-0:last-child {
        padding-bottom: 0
    }

    .hover\:text-franklin:hover {
        --tw-text-opacity: 1;
        color: rgb(60 255 208/var(--tw-text-opacity))
    }

    .dark .dark\:divide-gray-31 > :not([hidden]) ~ :not([hidden]) {
        --tw-divide-opacity: 1;
        border-color: rgb(49 49 49/var(--tw-divide-opacity))
    }

    .dark .dark\:marker\:text-franklin\/100 ::marker {
        color: #3cffd0
    }

    .dark .dark\:marker\:text-franklin ::marker {
        color: #3cffd0
    }

    .dark .dark\:selection\:bg-blurple ::-moz-selection {
        --tw-bg-opacity: 1;
        background-color: rgb(82 0 255/var(--tw-bg-opacity))
    }

    .dark .dark\:selection\:bg-blurple ::selection {
        --tw-bg-opacity: 1;
        background-color: rgb(82 0 255/var(--tw-bg-opacity))
    }

    @media (min-width: 640px) {

        .sm\:w-tablet-breaker {
            width: 410px
        }

    }

    @media (min-width: 768px) {
        .md\:left-6 {
            left: 6px
        }

        .md\:mb-40 {
            margin-bottom: 40px
        }

        .\[\&\>div\]\:md\:mb-\[88px\] > div {
            margin-bottom: 88px
        }

        .\[\&\>div\]\:last-of-type\:md\:border-b-0:last-of-type > div {
            border-bottom-width: 0
        }

        .md\:\[\&\>ul\]\:mb-0 > ul {
            margin-bottom: 0
        }
    }


    .\[\&_a\]\:relative a {
        position: relative
    }

    .\[\&_a\]\:z-10 a {
        z-index: 10
    }

    .\[\&_a\]\:font-semibold a {
        font-weight: 600
    }

    .\[\&_a\]\:font-medium a {
        font-weight: 500
    }

    .\[\&_a\]\:uppercase a {
        text-transform: uppercase
    }

    .\[\&_a\]\:tracking-6 a {
        letter-spacing: .06em
    }

    .\[\&_a\]\:text-gray-33 a {
        --tw-text-opacity: 1;
        color: rgb(51 51 51/var(--tw-text-opacity))
    }

    .\[\&_a\]\:text-black a {
        --tw-text-opacity: 1;
        color: rgb(0 0 0/var(--tw-text-opacity))
    }

    .\[\&_a\]\:text-white a {
        --tw-text-opacity: 1;
        color: rgb(255 255 255/var(--tw-text-opacity))
    }

    .\[\&_a\]\:text-blurple a {
        --tw-text-opacity: 1;
        color: rgb(82 0 255/var(--tw-text-opacity))
    }

    .\[\&_a\]\:shadow-underline-black a {
        --tw-shadow: inset 0 -1px 0 0 #000;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color)
    }

    .\[\&_a\]\:shadow-underline-black a, .\[\&_a\]\:shadow-underline-blurple a {
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .\[\&_a\]\:shadow-underline-blurple a {
        --tw-shadow: inset 0 -1px 0 0 #5200ff;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color)
    }

    .\[\&_a\]\:shadow-underline-gray-33 a {
        --tw-shadow: inset 0 -1px 0 0 #333;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color)
    }

    .\[\&_a\]\:shadow-underline-gray-33 a, .\[\&_a\]\:shadow-underline-white a {
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .\[\&_a\]\:shadow-underline-white a {
        --tw-shadow: inset 0 -1px 0 0 #fff;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color)
    }

    .dark .dark\:\[\&_a\]\:text-gray-ef a {
        --tw-text-opacity: 1;
        color: rgb(239 239 239/var(--tw-text-opacity))
    }

    .dark .dark\:\[\&_a\]\:shadow-underline-white a {
        --tw-shadow: inset 0 -1px 0 0 #fff;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .dark\:\[\&_a\]\:shadow-underline-franklin a {
        --tw-shadow: inset 0 -1px 0 0 #3cffd0;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .\[\&\>ul\]\:my-0 > ul {
        margin-top: 0;
        margin-bottom: 0
    }

    .\[\&\>ul\]\:mb-0 > ul {
        margin-bottom: 0
    }

    .\[\&\>ul\]\:mb-16 > ul {
        margin-bottom: 16px
    }

    .\[\&\>ul\]\:py-0 > ul {
        padding-top: 0;
        padding-bottom: 0
    }

    .\[\&\>ul\]\:pr-10 > ul {
        padding-right: 10px
    }

    .\[\&\>ul\>li\]\:mb-6 > ul > li {
        margin-bottom: 6px
    }

    .\[\&\>ul\>li\]\:leading-140 > ul > li {
        line-height: 1.4
    }

    @media (min-width: 1180px) {
        .lg\:\[\&\>ul\>li\]\:pl-10 > ul > li {
            padding-left: 10px
        }
    }

    .\[\&\>\*\:last-child\>\*\:last-child\]\:mb-0 > :last-child > :last-child {
        margin-bottom: 0
    }

    .\[\&\>blockquote\]\:my-20 > blockquote {
        margin-top: 20px;
        margin-bottom: 20px
    }

    .\[\&_\*\]\:mt-4 * {
        margin-top: 4px
    }

    .\[\&_\*\]\:mb-10 * {
        margin-bottom: 10px
    }

    .\[\&_\*\]\:ml-0 * {
        margin-left: 0
    }

    .\[\&_\*\]\:font-polysans-mono * {
        font-family: var(--font-polysans-mono)
    }

    .\[\&_\*\]\:text-14 * {
        font-size: 14px
    }

    @media (min-width: 1180px) {
        .\[\&_h2\]\:lg\:text-33 h2 {
            font-size: 33px
        }

        .\[\&_h3\]\:lg\:text-26 h3 {
            font-size: 26px
        }
    }

    .\[\&_h5\]\:text-black h5 {
        --tw-text-opacity: 1;
        color: rgb(0 0 0/var(--tw-text-opacity))
    }

    .\[\&_hr\]\:my-20 hr {
        margin-top: 20px;
        margin-bottom: 20px
    }

    .\[\&_ul\]\:py-0 ul {
        padding-top: 0;
        padding-bottom: 0
    }

    .\[\&_ul\]\:font-light ul {
        font-weight: 300
    }

    .\[\&_ol\]\:py-0 ol {
        padding-top: 0;
        padding-bottom: 0
    }

    .\[\&_li\]\:font-polysans li {
        font-family: var(--font-polysans)
    }

    .\[\&_li\]\:text-16 li {
        font-size: 16px
    }

    .\[\&_li\]\:font-light li {
        font-weight: 300
    }

    .\[\&_li\]\:leading-130 li {
        line-height: 1.3
    }

    .\[\&_li\]\:marker\:text-franklin * li::marker {
        color: #3cffd0
    }

    .\[\&_li\]\:marker\:text-franklin li::marker {
        color: #3cffd0
    }

    .\[\&_p\]\:font-polysans p {
        font-family: var(--font-polysans)
    }

    .\[\&_p\]\:text-16 p {
        font-size: 16px
    }

    .\[\&_p\]\:font-light p {
        font-weight: 300
    }

    .\[\&_p\]\:leading-130 p {
        line-height: 1.3
    }

    .\[\&_a\:hover\]\:text-blurple a:hover {
        --tw-text-opacity: 1;
        color: rgb(82 0 255/var(--tw-text-opacity))
    }

    .\[\&_a\:hover\]\:underline a:hover {
        text-decoration-line: underline
    }

    .\[\&_a\:hover\]\:shadow-highlight-franklin a:hover {
        --tw-shadow: inset 0 -.5em 0 0 #3cffd0;
        --tw-shadow-colored: inset 0 -.5em 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .\[\&_a\:hover\]\:shadow-underline-blurple a:hover {
        --tw-shadow: inset 0 -1px 0 0 #5200ff;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .\[\&_a\:hover\]\:shadow-highlight-blurple a:hover {
        --tw-shadow: inset 0 -.5em 0 0 #5200ff;
        --tw-shadow-colored: inset 0 -.5em 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .dark\:\[\&_a\:hover\]\:text-franklin a:hover {
        --tw-text-opacity: 1;
        color: rgb(60 255 208/var(--tw-text-opacity))
    }

    .dark .dark\:\[\&_a\:hover\]\:shadow-highlight-blurple a:hover {
        --tw-shadow: inset 0 -.5em 0 0 #5200ff;
        --tw-shadow-colored: inset 0 -.5em 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .dark\:\[\&_a\:hover\]\:shadow-underline-franklin a:hover {
        --tw-shadow: inset 0 -1px 0 0 #3cffd0;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .dark\:\[\&_a\:hover\]\:shadow-highlight-franklin a:hover {
        --tw-shadow: inset 0 -.5em 0 0 #3cffd0;
        --tw-shadow-colored: inset 0 -.5em 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .\[\&\>span\]\:rounded-\[2px\] > span {
        border-radius: 2px
    }

    .\[\&\>div\>hr\]\:last\:border-none:last-child > div > hr {
        border-style: none
    }

    .\[\&\>\*\>li\]\:text-blurple > * > li {
        --tw-text-opacity: 1;
        color: rgb(82 0 255/var(--tw-text-opacity))
    }

    .dark .dark\:\[\&\>\*\>li\]\:text-franklin > * > li {
        --tw-text-opacity: 1;
        color: rgb(60 255 208/var(--tw-text-opacity))
    }

    .\[\&\>iframe\]\:absolute > iframe {
        position: absolute
    }

    .\[\&\>iframe\]\:h-full > iframe {
        height: 100%
    }

    .\[\&\>iframe\]\:w-full > iframe {
        width: 100%
    }

    .\[\&\>video\]\:absolute > video {
        position: absolute
    }

    .\[\&\>video\]\:h-full > video {
        height: 100%
    }

    .\[\&\>video\]\:w-full > video {
        width: 100%
    }

    .\[\&\>p\>span\:first-child\]\:text-black > p > span:first-child {
        --tw-text-opacity: 1;
        color: rgb(0 0 0/var(--tw-text-opacity))
    }

    .\[\&\>p\>span\:first-child\]\:text-gray-13 > p > span:first-child {
        --tw-text-opacity: 1;
        color: rgb(19 19 19/var(--tw-text-opacity))
    }

    .\[\&_svg\]\:drop-shadow-meatball svg {
        --tw-drop-shadow: drop-shadow(0px -8px 8px #131313) drop-shadow(0px 8px 8px #131313);
        filter: var(--tw-blur) var(--tw-brightness) var(--tw-contrast) var(--tw-grayscale) var(--tw-hue-rotate) var(--tw-invert) var(--tw-saturate) var(--tw-sepia) var(--tw-drop-shadow)
    }

    .\[\&\>time\]\:leading-120 > time {
        line-height: 1.2
    }

    @media (min-width: 1180px) {
        .\[\&\>time\]\:lg\:block > time {
            display: block
        }

        .lg\:\[\&_figcaption\]\:text-gray-13 figcaption {
            --tw-text-opacity: 1;
            color: rgb(19 19 19/var(--tw-text-opacity))
        }

        .lg\:\[\&_cite\]\:text-gray-4a cite {
            --tw-text-opacity: 1;
            color: rgb(74 74 74/var(--tw-text-opacity))
        }
    }

    .\[\&\>a\:hover\]\:text-black > a:hover {
        --tw-text-opacity: 1;
        color: rgb(0 0 0/var(--tw-text-opacity))
    }

    .\[\&\>a\:hover\]\:text-gray-63 > a:hover {
        --tw-text-opacity: 1;
        color: rgb(99 99 99/var(--tw-text-opacity))
    }

    .\[\&\>a\:hover\]\:shadow-highlight-franklin > a:hover {
        --tw-shadow: inset 0 -.5em 0 0 #3cffd0;
        --tw-shadow-colored: inset 0 -.5em 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .\[\&\>a\:hover\]\:shadow-underline-black > a:hover {
        --tw-shadow: inset 0 -1px 0 0 #000;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .dark\:\[\&\>a\:hover\]\:text-gray-e9 > a:hover {
        --tw-text-opacity: 1;
        color: rgb(233 233 233/var(--tw-text-opacity))
    }

    .dark .dark\:\[\&\>a\:hover\]\:text-gray-bd > a:hover {
        --tw-text-opacity: 1;
        color: rgb(189 189 189/var(--tw-text-opacity))
    }

    .dark .dark\:\[\&\>a\:hover\]\:shadow-highlight-franklin > a:hover {
        --tw-shadow: inset 0 -.5em 0 0 #3cffd0;
        --tw-shadow-colored: inset 0 -.5em 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .dark\:\[\&\>a\:hover\]\:shadow-underline-gray-63 > a:hover {
        --tw-shadow: inset 0 -1px 0 0 #636363;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .dark\:\[\&\>a\:hover\]\:shadow-underline-gray > a:hover {
        --tw-shadow: inset 0 -1px 0 0 #bdbdbd;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .\[\&\>p\]\:mb-8 > p {
        margin-bottom: 8px
    }

    .\[\&_strong\]\:font-medium strong {
        font-weight: 500
    }

    @font-face {
        font-family: __fkRomanStandard_3b2615;
        src: url(/eks-assets/_next/static/media/b61d461e2e1d8573-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 400;
        font-style: normal
    }

    @font-face {
        font-family: __fkRomanStandard_3b2615;
        src: url(/eks-assets/_next/static/media/af51b8e80b7e5b97-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 400;
        font-style: italic
    }

    @font-face {
        font-family: __fkRomanStandard_3b2615;
        src: url(/eks-assets/_next/static/media/4c161430243654b9-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 700;
        font-style: normal
    }

    @font-face {
        font-family: __fkRomanStandard_3b2615;
        src: url(/eks-assets/_next/static/media/faa4a7ab7fe4ff34-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 700;
        font-style: italic
    }

    @font-face {
        font-family: __fkRomanStandard_Fallback_3b2615;
        src: local("Times New Roman");
        ascent-override: 80.77%;
        descent-override: 26.92%;
        line-gap-override: 0.00%;
        size-adjust: 118.86%
    }

    @font-face {
        font-family: __manuka_e627f3;
        src: url(/eks-assets/_next/static/media/e0d450417c4fcdb2-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 900;
        font-style: normal
    }

    @font-face {
        font-family: __manuka_e627f3;
        src: url(/eks-assets/_next/static/media/c6806ee6b9a6284f-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 1000;
        font-style: normal
    }

    @font-face {
        font-family: __manuka_Fallback_e627f3;
        src: local("Arial");
        ascent-override: 184.06%;
        descent-override: 25.82%;
        line-gap-override: 0.00%;
        size-adjust: 48.41%
    }

    @font-face {
        font-family: __polySans_5fdfbc;
        src: url(/eks-assets/_next/static/media/167de315d6f8820c-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 300;
        font-style: normal
    }

    @font-face {
        font-family: __polySans_5fdfbc;
        src: url(/eks-assets/_next/static/media/c32d4f9e62509b70-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 300;
        font-style: italic
    }

    @font-face {
        font-family: __polySans_5fdfbc;
        src: url(/eks-assets/_next/static/media/8314bd48671746e7-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 400;
        font-style: normal
    }

    @font-face {
        font-family: __polySans_5fdfbc;
        src: url(/eks-assets/_next/static/media/1acdcb23bd60cdf8-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 400;
        font-style: italic
    }

    @font-face {
        font-family: __polySans_5fdfbc;
        src: url(/eks-assets/_next/static/media/e334064d2786be51-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 500;
        font-style: normal
    }

    @font-face {
        font-family: __polySans_5fdfbc;
        src: url(/eks-assets/_next/static/media/dbe24bfb7e9bcd79-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 500;
        font-style: italic
    }

    @font-face {
        font-family: __polySans_5fdfbc;
        src: url(/eks-assets/_next/static/media/caa65695070c604f-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 700;
        font-style: normal
    }

    @font-face {
        font-family: __polySans_5fdfbc;
        src: url(/eks-assets/_next/static/media/7f8638c9585902a6-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 700;
        font-style: italic
    }

    @font-face {
        font-family: __polySans_Fallback_5fdfbc;
        src: local("Arial");
        ascent-override: 95.01%;
        descent-override: 18.10%;
        line-gap-override: 0.00%;
        size-adjust: 106.09%
    }

    @font-face {
        font-family: __polySansMono_8812cd;
        src: url(/eks-assets/_next/static/media/d2cd5f6e542bad4c-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 300;
        font-style: normal
    }

    @font-face {
        font-family: __polySansMono_8812cd;
        src: url(/eks-assets/_next/static/media/857aa1a339c7fe20-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 300;
        font-style: italic
    }

    @font-face {
        font-family: __polySansMono_8812cd;
        src: url(/eks-assets/_next/static/media/516340c748fee9da-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 400;
        font-style: normal
    }

    @font-face {
        font-family: __polySansMono_8812cd;
        src: url(/eks-assets/_next/static/media/70754f98ca969379-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 400;
        font-style: italic
    }

    @font-face {
        font-family: __polySansMono_8812cd;
        src: url(/eks-assets/_next/static/media/afa7a955b67174eb-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 500;
        font-style: normal
    }

    @font-face {
        font-family: __polySansMono_8812cd;
        src: url(/eks-assets/_next/static/media/d2ddd5a6c0493c79-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 500;
        font-style: italic
    }

    @font-face {
        font-family: __polySansMono_8812cd;
        src: url(/eks-assets/_next/static/media/60369a8d37d9d5b8-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 700;
        font-style: normal
    }

    @font-face {
        font-family: __polySansMono_8812cd;
        src: url(/eks-assets/_next/static/media/96fec850ad729c00-s.p.woff2) format("woff2");
        font-display: swap;
        font-weight: 700;
        font-style: italic
    }

    @font-face {
        font-family: __polySansMono_Fallback_8812cd;
        src: local("Arial");
        ascent-override: 75.65%;
        descent-override: 14.41%;
        line-gap-override: 0.00%;
        size-adjust: 133.24%
    }
</style>


<!--<section class="mx-auto flex max-w-4xl w-full flex-col items-start justify-center ">-->

<!--    <div class="w-full flex flex-col md:flex-row gap-y-2 md:gap-y-0 gap-x-2">-->


<!--        <div class="relative flex flex-col items-center w-full md:w-2/3 md:flex-row bg-yellow dark:bg-yellow-dark border-grey-900 dark:border-0 border-2 rounded-lg overflow-hidden">-->
<!--            <div class="flex flex-1">-->
<!--                <div class="block md:hidden self-center m-auto">-->
<!--                </div>-->
<!--            </div>-->
<!--        </div>-->


<!--        <div class="bg-blue dark:bg-blue-300 w-full lg:w-1/3 lg:min-w-550px border-2 border-grey-900 rounded-xl flex flex-col justify-between align-center p-6">-->
<!--            <h2 class="sm:s-h3 md:l-h3 w-5/6 text-grey-900 font-medium">-->
<!--                And that's a wrap!-->
<!--                <br>-->
<!--                Thanks for joining Google I/O 2022.-->
<!--            </h2>-->
<!--            <div class="pt-20">-->


<!--                <div class="h-external-link" data-id="home_recapmodule_cta_io2022recap" data-styles="underline sm:l-p1 md:l-p1 text-grey-900 mt-4 md:mt-0 md:mb-4 " data-aria="home_recapmodule_headline_io2022recap" data-alt=""><p><a href="https://www.youtube.com/watch?v=CWTm0ccfZe4&amp;list=TLGGLYR0fesogp0xMjA1MjAyMg" rel="noreferrer" target="_blank" aria-label="I/O '22 recap" class="underline sm:l-p1 md:l-p1 text-grey-900 mt-4 md:mt-0 md:mb-4">Watch the I/O 2022 recap</a></p><span></span></div>-->

<!--            </div>-->
<!--        </div>-->
<!--    </div>-->


<!--</section>-->



