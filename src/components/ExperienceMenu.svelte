<script>
    export let experience;
    export let title;
    export let style;

    function scrollIntoView({target}) {
        const el = document.querySelector(target.getAttribute('href'));
        if (!el) return;


        el.scrollIntoView({
            block: "start", inline: "nearest",
            behavior: 'smooth'
        });
    }
</script>

<div class="p-8 lg:w-1/2 lg:p-20">
    <div class="lg:sticker top-48 py-8 lg:sticky lg:py-20">
        <div id='card'
             style={style}
             class="duet--recirculation--list-breaker-compact ml:m-auto relative mt-80 ml-[65px] min-h-[475px] w-mobile-breaker  rounded-[4px] p-20 sm:w-tablet-breaker md:mb-40  lg:sticky lg:top-40 lg:mt-0  lg:ml-0 lg:min-h-[600px] lg:w-desktop-breaker lg:overflow-hidden lg:rounded-[20px] bg-blurple/90 text-white">
            <h2 class="absolute top-[-25px] left-[-80px] -z-10 flex rotate-180 font-manuka text-[110px] font-ultra leading-100 tracking-1 text-gray-900 dark:text-white lg:hidden"
                style="writing-mode: vertical-rl; text-orientation: sideways;">{title}</h2>
            <div class="text-9 relative z-10 mb-20 flex justify-between font-polysans  text-10 uppercase tracking-15">
                <span class="font-medium">{title}</span></div>
            <div class="absolute right-0 bottom-[-10px] mr-[-25px] hidden h-full rotate-180 font-manuka text-[190px] font-ultra  leading-100 lg:flex text-blurple-39"
                 style="writing-mode: vertical-rl; text-orientation: sideways;">{title}
            </div>
            <ol class="styled-counter w-full lg:mt-20 lg:w-[320px] styled-counter-compact">
                {#each experience as item, i}
                    <li class="mb-20 border-b pb-20 text-franklin last:mb-0 last:border-0 last:pb-0 lg:last:mb-20 border-b-franklin">
                        <a class="text-white hover:text-franklin mb-4 font-polysans text-18 font-medium leading-110 tracking-1"
                           on:click|preventDefault={scrollIntoView}
                           href={item.href}>
                            {item.title}
                        </a>
                        <p class="duet--recirculation--breaker-byline font-polysans text-11 uppercase leading-140 tracking-15">
                            <span class="mr-8 text-gray-ef">{item.startedAt}</span>
                            <span
                                class="mr-8 font-light text-gray-ef">{item.endedAt}</span></p>
                    </li>
                {/each}
            </ol>
        </div>
    </div>
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

    .z-0 {
        z-index: 0
    }

    .-z-10 {
        z-index: -10
    }

    .mx-auto {
        margin-left: auto;
        margin-right: auto
    }

    .mx-10 {
        margin-left: 10px;
        margin-right: 10px
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

    .ml-10 {
        margin-left: 10px
    }

    .mr-20 {
        margin-right: 20px
    }

    .mt-12 {
        margin-top: 12px
    }

    .mt-8 {
        margin-top: 8px
    }

    .mb-6 {
        margin-bottom: 6px
    }

    .ml-0 {
        margin-left: 0
    }

    .mt-2 {
        margin-top: 2px
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

    .inline-block {
        display: inline-block
    }

    .inline {
        display: inline
    }

    .flex {
        display: flex
    }

    .hidden {
        display: none
    }

    .aspect-square {
        aspect-ratio: 1/1
    }

    .aspect-standard {
        aspect-ratio: 3/2
    }

    .h-full {
        height: 100%
    }

    .h-24 {
        height: 24px
    }

    .h-12 {
        height: 12px
    }

    .h-1\/3 {
        height: 33.333333%
    }

    .h-\[45px\] {
        height: 45px
    }

    .min-h-\[475px\] {
        min-height: 475px
    }

    .min-h-\[31px\] {
        min-height: 31px
    }

    .w-full {
        width: 100%
    }

    .w-\[75px\] {
        width: 75px
    }

    .w-24 {
        width: 24px
    }

    .w-12 {
        width: 12px
    }

    .w-\[320px\] {
        width: 320px
    }

    .w-\[45px\] {
        width: 45px
    }

    .w-mobile-breaker {
        width: 300px
    }

    .w-60 {
        width: 60px
    }

    .min-w-0 {
        min-width: 0
    }

    .min-w-\[38px\] {
        min-width: 38px
    }

    .max-w-container-sm {
        max-width: 500px
    }

    .max-w-content-block-mobile {
        max-width: 260px
    }

    .max-w-\[400px\] {
        max-width: 400px
    }

    .max-w-desktop-breaker {
        max-width: 650px
    }

    .max-w-\[560px\] {
        max-width: 560px
    }

    .flex-auto {
        flex: 1 1 auto
    }

    .flex-1 {
        flex: 1 1 0%
    }

    .translate-y-0 {
        --tw-translate-y: 0px
    }

    .-translate-x-1\/2 {
        --tw-translate-x: -50%
    }

    .-rotate-180 {
        --tw-rotate: -180deg
    }

    .-rotate-180, .rotate-180 {
        transform: translate(var(--tw-translate-x), var(--tw-translate-y)) rotate(var(--tw-rotate)) skewX(var(--tw-skew-x)) skewY(var(--tw-skew-y)) scaleX(var(--tw-scale-x)) scaleY(var(--tw-scale-y))
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

    .flex-row {
        flex-direction: row
    }

    .flex-col {
        flex-direction: column
    }

    .flex-wrap {
        flex-wrap: wrap
    }

    .items-center {
        align-items: center
    }

    .justify-center {
        justify-content: center
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

    .rounded-sm {
        border-radius: .125rem
    }

    .rounded-full {
        border-radius: 9999px
    }

    .rounded-\[2px\] {
        border-radius: 2px
    }

    .rounded-\[3px\] {
        border-radius: 3px
    }

    .rounded-\[4px\] {
        border-radius: 4px
    }

    .border-b {
        border-bottom-width: 1px
    }

    .border-l {
        border-left-width: 1px
    }

    .border-t-\[3px\] {
        border-top-width: 3px
    }

    .border-solid {
        border-style: solid
    }

    .border-gray-cc {
        --tw-border-opacity: 1;
        border-color: rgb(204 204 204/var(--tw-border-opacity))
    }

    .border-franklin {
        --tw-border-opacity: 1;
        border-color: rgb(60 255 208/var(--tw-border-opacity))
    }

    .border-blurple {
        --tw-border-opacity: 1;
        border-color: rgb(82 0 255/var(--tw-border-opacity))
    }

    .border-gray-bd {
        --tw-border-opacity: 1;
        border-color: rgb(189 189 189/var(--tw-border-opacity))
    }

    .border-b-franklin {
        --tw-border-opacity: 1;
        border-bottom-color: rgb(60 255 208/var(--tw-border-opacity))
    }

    .border-b-blurple {
        --tw-border-opacity: 1;
        border-bottom-color: rgb(82 0 255/var(--tw-border-opacity))
    }

    .border-l-blurple {
        --tw-border-opacity: 1;
        border-left-color: rgb(82 0 255/var(--tw-border-opacity))
    }

    .bg-white {
        --tw-bg-opacity: 1;
        background-color: rgb(255 255 255/var(--tw-bg-opacity))
    }

    .bg-gray-13 {
        --tw-bg-opacity: 1;
        background-color: rgb(19 19 19/var(--tw-bg-opacity))
    }

    .bg-black\/50 {
        background-color: rgba(0, 0, 0, .5)
    }

    .bg-blurple\/90 {
        background-color: rgba(82, 0, 255, .9)
    }

    .bg-gray-bd {
        --tw-bg-opacity: 1;
        background-color: rgb(189 189 189/var(--tw-bg-opacity))
    }

    .bg-gradient-to-t {
        background-image: linear-gradient(to top, var(--tw-gradient-stops))
    }

    .from-black\/10 {
        --tw-gradient-from: rgba(0, 0, 0, .1);
        --tw-gradient-to: transparent;
        --tw-gradient-stops: var(--tw-gradient-from), var(--tw-gradient-to)
    }

    .from-black\/30 {
        --tw-gradient-from: rgba(0, 0, 0, .3);
        --tw-gradient-to: transparent;
        --tw-gradient-stops: var(--tw-gradient-from), var(--tw-gradient-to)
    }

    .to-transparent {
        --tw-gradient-to: transparent
    }

    .fill-gray-63 {
        fill: #636363
    }

    .p-20 {
        padding: 20px
    }

    .p-\[5px\] {
        padding: 5px
    }

    .py-6 {
        padding-top: 6px;
        padding-bottom: 6px
    }

    .px-0 {
        padding-left: 0;
        padding-right: 0
    }

    .py-16 {
        padding-top: 16px;
        padding-bottom: 16px
    }

    .px-4 {
        padding-left: 4px;
        padding-right: 4px
    }

    .pt-12 {
        padding-top: 12px
    }

    .pb-20 {
        padding-bottom: 20px
    }

    .pt-4 {
        padding-top: 4px
    }

    .pb-4 {
        padding-bottom: 4px
    }

    .pb-16 {
        padding-bottom: 16px
    }

    .pb-40 {
        padding-bottom: 40px
    }

    .pl-4 {
        padding-left: 4px
    }

    .pt-\[12px\] {
        padding-top: 12px
    }

    .pr-12 {
        padding-right: 12px
    }

    .pt-28 {
        padding-top: 28px
    }

    .pr-4 {
        padding-right: 4px
    }

    .pt-6 {
        padding-top: 6px
    }

    .pl-\[38px\] {
        padding-left: 38px
    }

    .text-center {
        text-align: center
    }

    .font-polysans {
        font-family: var(--font-polysans)
    }

    .font-manuka {
        font-family: var(--font-manuka)
    }

    .font-polysans-mono {
        font-family: var(--font-polysans-mono)
    }

    .font-fkroman {
        font-family: var(--font-fkroman)
    }

    .text-18 {
        font-size: 18px
    }

    .text-20 {
        font-size: 20px
    }

    .text-12 {
        font-size: 12px
    }

    .text-30 {
        font-size: 30px
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

    .font-bold {
        font-weight: 700
    }

    .font-normal {
        font-weight: 400
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

    .not-italic {
        font-style: normal
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

    .leading-130 {
        line-height: 1.3
    }

    .leading-none {
        line-height: 1
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

    .tracking-normal {
        letter-spacing: 0
    }

    .text-black {
        --tw-text-opacity: 1;
        color: rgb(0 0 0/var(--tw-text-opacity))
    }

    .text-blurple {
        --tw-text-opacity: 1;
        color: rgb(82 0 255/var(--tw-text-opacity))
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

    .text-gray-33 {
        --tw-text-opacity: 1;
        color: rgb(51 51 51/var(--tw-text-opacity))
    }

    .text-gray-31 {
        --tw-text-opacity: 1;
        color: rgb(49 49 49/var(--tw-text-opacity))
    }

    .text-gray-63 {
        --tw-text-opacity: 1;
        color: rgb(99 99 99/var(--tw-text-opacity))
    }

    .text-gray-4a {
        --tw-text-opacity: 1;
        color: rgb(74 74 74/var(--tw-text-opacity))
    }

    .text-gray-ef {
        --tw-text-opacity: 1;
        color: rgb(239 239 239/var(--tw-text-opacity))
    }

    .text-blurple-39 {
        --tw-text-opacity: 1;
        color: rgb(57 4 171/var(--tw-text-opacity))
    }

    .shadow-underline-blurple {
        --tw-shadow: inset 0 -1px 0 0 #5200ff;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color)
    }

    .transition {
        transition-property: color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, -webkit-backdrop-filter;
        transition-property: color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter;
        transition-property: color, background-color, border-color, text-decoration-color, fill, stroke, opacity, box-shadow, transform, filter, backdrop-filter, -webkit-backdrop-filter;
        transition-timing-function: cubic-bezier(.4, 0, .2, 1);
        transition-duration: .15s
    }

    .m-ad {
        line-height: 0;
        overflow: hidden;
        text-align: center;
        margin-left: auto;
        margin-right: auto
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

    [data-concert=leaderboard_top_tablet_desktop] .m-ad {
        width: 100%
    }

    .bg-black .m-ad, .bg-black ~ .m-ad, .duet--page-layout--hub .m-ad {
        background-color: #000
    }

    .duet--layout--blurple-header .m-ad {
        background-color: transparent
    }

    .dynamic-js-slot:before {
        transition: opacity .15s
    }

    .dfp_ad--held-area {
        border: 1px solid hsla(0, 0%, 98%, 0);
        overflow: hidden;
        margin-left: auto;
        margin-right: auto;
        position: relative
    }

    .dfp_ad--held-area:before {
        content: "AD";
        position: absolute;
        width: 100%;
        transform: translateY(-50%);
        top: 50%;
        left: 0;
        text-align: center;
        font-size: 16px;
        color: hsla(0, 0%, 98%, 0);
        opacity: 1;
        z-index: 1
    }

    .dfp_ad--held-area > div {
        z-index: 2;
        position: relative
    }

    [data-concert-ads-athena-max-size="1060"] .dynamic-js-slot {
        max-width: 1060px;
        width: 100%
    }

    @media only screen and (max-width: 767px) {
    }

    .dfp_ad--full-width {
        margin-top: 40px;
        margin-bottom: 40px
    }

    @media (min-width: 768px) {
    }

    @media (min-width: 1181px) {
        .dfp_ad--full-width {
            margin-top: 80px;
            margin-bottom: 80px
        }
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

    .before\:relative:before {
        content: var(--tw-content);
        position: relative
    }

    .before\:top-\[50\%\]:before {
        content: var(--tw-content);
        top: 50%
    }

    .before\:m-auto:before {
        content: var(--tw-content);
        margin: auto
    }

    .before\:flex:before {
        content: var(--tw-content);
        display: flex
    }

    .before\:h-\[6px\]:before {
        content: var(--tw-content);
        height: 6px
    }

    .before\:w-\[300px\]:before {
        content: var(--tw-content);
        width: 300px
    }

    .before\:bg-gray-cc:before {
        content: var(--tw-content);
        --tw-bg-opacity: 1;
        background-color: rgb(204 204 204/var(--tw-bg-opacity))
    }

    .before\:content-\[\'\'\]:before {
        --tw-content: "";
        content: var(--tw-content)
    }

    .after\:absolute:after {
        content: var(--tw-content);
        position: absolute
    }

    .after\:inset-0:after {
        content: var(--tw-content);
        top: 0;
        right: 0;
        bottom: 0;
        left: 0
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

    .last-of-type\:border-b-0:last-of-type {
        border-bottom-width: 0
    }

    .hover\:bg-\[\#FBF9FF\]:hover {
        --tw-bg-opacity: 1;
        background-color: rgb(251 249 255/var(--tw-bg-opacity))
    }

    .hover\:fill-black:hover {
        fill: #000
    }

    .hover\:text-blurple:hover {
        --tw-text-opacity: 1;
        color: rgb(82 0 255/var(--tw-text-opacity))
    }

    .hover\:text-franklin:hover {
        --tw-text-opacity: 1;
        color: rgb(60 255 208/var(--tw-text-opacity))
    }

    .hover\:shadow-underline-inherit:hover {
        --tw-shadow: inset 0 -1px 0 0;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color)
    }

    .hover\:shadow-underline-blurple:hover, .hover\:shadow-underline-inherit:hover {
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .hover\:shadow-underline-blurple:hover {
        --tw-shadow: inset 0 -1px 0 0 #5200ff;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color)
    }

    .group:hover .group-hover\:bg-black {
        --tw-bg-opacity: 1;
        background-color: rgb(0 0 0/var(--tw-bg-opacity))
    }

    .group:hover .group-hover\:shadow-highlight-franklin {
        --tw-shadow: inset 0 -.5em 0 0 #3cffd0;
        --tw-shadow-colored: inset 0 -.5em 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .group:hover .group-hover\:shadow-underline-blurple {
        --tw-shadow: inset 0 -1px 0 0 #5200ff;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .dark\:absolute {
        position: absolute
    }

    .dark .dark\:divide-gray-31 > :not([hidden]) ~ :not([hidden]) {
        --tw-divide-opacity: 1;
        border-color: rgb(49 49 49/var(--tw-divide-opacity))
    }

    .dark .dark\:border-b-8 {
        border-bottom-width: 8px
    }

    .dark .dark\:border-none {
        border-style: none
    }

    .dark .dark\:border-gray-31 {
        --tw-border-opacity: 1;
        border-color: rgb(49 49 49/var(--tw-border-opacity))
    }

    .dark .dark\:border-gray-4a {
        --tw-border-opacity: 1;
        border-color: rgb(74 74 74/var(--tw-border-opacity))
    }

    .dark .dark\:border-b-franklin {
        --tw-border-opacity: 1;
        border-bottom-color: rgb(60 255 208/var(--tw-border-opacity))
    }

    .dark .dark\:border-b-gray-31 {
        --tw-border-opacity: 1;
        border-bottom-color: rgb(49 49 49/var(--tw-border-opacity))
    }

    .dark .dark\:border-l-franklin {
        --tw-border-opacity: 1;
        border-left-color: rgb(60 255 208/var(--tw-border-opacity))
    }

    .dark .dark\:bg-gray-13 {
        --tw-bg-opacity: 1;
        background-color: rgb(19 19 19/var(--tw-bg-opacity))
    }

    .dark .dark\:bg-transparent {
        background-color: transparent
    }

    .dark .dark\:bg-\[\#313131\] {
        --tw-bg-opacity: 1;
        background-color: rgb(49 49 49/var(--tw-bg-opacity))
    }

    .dark .dark\:text-white {
        --tw-text-opacity: 1;
        color: rgb(255 255 255/var(--tw-text-opacity))
    }

    .dark .dark\:text-franklin {
        --tw-text-opacity: 1;
        color: rgb(60 255 208/var(--tw-text-opacity))
    }

    .dark .dark\:text-gray-bd {
        --tw-text-opacity: 1;
        color: rgb(189 189 189/var(--tw-text-opacity))
    }

    .dark .dark\:text-gray-94 {
        --tw-text-opacity: 1;
        color: rgb(148 148 148/var(--tw-text-opacity))
    }

    .dark .dark\:text-gray-ef {
        --tw-text-opacity: 1;
        color: rgb(239 239 239/var(--tw-text-opacity))
    }

    .dark .dark\:text-gray-cc {
        --tw-text-opacity: 1;
        color: rgb(204 204 204/var(--tw-text-opacity))
    }

    .dark .dark\:shadow-underline-franklin {
        --tw-shadow: inset 0 -1px 0 0 #3cffd0;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
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

    .dark .dark\:before\:bg-gray-31:before {
        content: var(--tw-content);
        --tw-bg-opacity: 1;
        background-color: rgb(49 49 49/var(--tw-bg-opacity))
    }

    .dark .dark\:hover\:bg-gray-18:hover {
        --tw-bg-opacity: 1;
        background-color: rgb(24 24 24/var(--tw-bg-opacity))
    }

    .dark .dark\:hover\:fill-white:hover {
        fill: #fff
    }

    .dark .dark\:hover\:text-franklin:hover {
        --tw-text-opacity: 1;
        color: rgb(60 255 208/var(--tw-text-opacity))
    }

    .dark .dark\:hover\:shadow-underline-franklin:hover {
        --tw-shadow: inset 0 -1px 0 0 #3cffd0;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .group:hover .dark\:group-hover\:shadow-highlight-blurple {
        --tw-shadow: inset 0 -.5em 0 0 #5200ff;
        --tw-shadow-colored: inset 0 -.5em 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .group:hover .dark\:group-hover\:shadow-underline-franklin {
        --tw-shadow: inset 0 -1px 0 0 #3cffd0;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    @media (min-width: 640px) {
        .sm\:ml-auto {
            margin-left: auto
        }

        .sm\:ml-10 {
            margin-left: 10px
        }

        .sm\:mr-10 {
            margin-right: 10px
        }

        .sm\:w-\[480px\] {
            width: 480px
        }

        .sm\:w-\[440px\] {
            width: 440px
        }

        .sm\:w-content-block-compact {
            width: 320px
        }

        .sm\:w-\[100px\] {
            width: 100px
        }

        .sm\:w-tablet-breaker {
            width: 410px
        }

        .sm\:max-w-container-sm {
            max-width: 500px
        }

        .sm\:max-w-content-block-compact {
            max-width: 320px
        }

        .sm\:px-\[16px\] {
            padding-left: 16px;
            padding-right: 16px
        }

        .sm\:text-35 {
            font-size: 35px
        }
    }

    @media (min-width: 768px) {
        .md\:left-6 {
            left: 6px
        }

        .md\:mx-auto {
            margin-left: auto;
            margin-right: auto
        }

        .md\:mb-40 {
            margin-bottom: 40px
        }

        .md\:ml-\[-3px\] {
            margin-left: -3px
        }

        .md\:block {
            display: block
        }

        .md\:hidden {
            display: none
        }

        .md\:max-w-\[560px\] {
            max-width: 560px
        }

        .md\:flex-row {
            flex-direction: row
        }

        .md\:items-start {
            align-items: flex-start
        }

        .md\:justify-start {
            justify-content: flex-start
        }

        .md\:px-10 {
            padding-left: 10px;
            padding-right: 10px
        }

        .md\:text-24 {
            font-size: 24px
        }

        .md\:text-17 {
            font-size: 17px
        }

        .md\:before\:w-\[728px\]:before {
            content: var(--tw-content);
            width: 728px
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

    @media (min-width: 1180px) {
        .lg\:sticky {
            position: sticky
        }

        .lg\:top-40 {
            top: 40px
        }

        .lg\:left-16 {
            left: 16px
        }

        .lg\:mr-100 {
            margin-right: 100px
        }

        .lg\:mb-8 {
            margin-bottom: 8px
        }

        .lg\:mb-0 {
            margin-bottom: 0
        }

        .lg\:ml-0 {
            margin-left: 0
        }

        .lg\:mt-0 {
            margin-top: 0
        }

        .lg\:mt-20 {
            margin-top: 20px
        }

        .lg\:ml-50 {
            margin-left: 50px
        }

        .lg\:block {
            display: block
        }

        .lg\:flex {
            display: flex
        }

        .lg\:hidden {
            display: none
        }

        .lg\:min-h-\[600px\] {
            min-height: 600px
        }

        .lg\:w-desktop-breaker {
            width: 500px
        }

        .lg\:w-\[320px\] {
            width: 320px
        }

        .lg\:max-w-container-lg {
            max-width: 1100px
        }

        .lg\:flex-1 {
            flex: 1 1 0%
        }

        .lg\:flex-row {
            flex-direction: row
        }

        .lg\:flex-col {
            flex-direction: column
        }

        .lg\:items-start {
            align-items: flex-start
        }

        .lg\:self-stretch {
            align-self: stretch
        }

        .lg\:overflow-hidden {
            overflow: hidden
        }

        .lg\:rounded-\[20px\] {
            border-radius: 20px
        }

        .lg\:py-24 {
            padding-top: 24px;
            padding-bottom: 24px
        }

        .lg\:py-30 {
            padding-top: 30px;
            padding-bottom: 30px
        }

        .lg\:py-20 {
            padding-top: 20px;
            padding-bottom: 20px
        }

        .lg\:pt-40 {
            padding-top: 40px
        }

        .lg\:pl-50 {
            padding-left: 50px
        }

        .lg\:last\:mb-20:last-child {
            margin-bottom: 20px
        }
    }

    .\[\&\>b\]\:font-medium > b {
        font-weight: 500
    }

    .\[\&\>b\]\:text-blurple > b {
        --tw-text-opacity: 1;
        color: rgb(82 0 255/var(--tw-text-opacity))
    }

    .dark .dark\:\[\&\>b\]\:text-franklin > b {
        --tw-text-opacity: 1;
        color: rgb(60 255 208/var(--tw-text-opacity))
    }

    .\[\&\>div\]\:mb-28 > div {
        margin-bottom: 28px
    }

    .\[\&\>div\]\:border-b > div {
        border-bottom-width: 1px
    }

    .\[\&\>div\]\:border-black\/30 > div {
        border-color: rgba(0, 0, 0, .3)
    }

    .\[\&\>div\]\:last\:border-b-0:last-child > div {
        border-bottom-width: 0
    }

    .\[\&\>div\]\:last\:border-l-0:last-child > div {
        border-left-width: 0
    }

    .\[\&\>div\]\:first-of-type\:mt-0:first-of-type > div {
        margin-top: 0
    }

    .\[\&\>div\]\:first-of-type\:pt-0:first-of-type > div {
        padding-top: 0
    }

    .\[\&\>div\]\:last-of-type\:pb-0:last-of-type > div {
        padding-bottom: 0
    }

    @media (min-width: 1180px) {
        .lg\:\[\&\>div\]\:border-none > div {
            border-style: none
        }

        .lg\:\[\&\>div\]\:bg-gray-13\/80 > div {
            background-color: hsla(0, 0%, 7%, .8)
        }
    }

    .\[\&\>a\]\:font-semibold > a {
        font-weight: 600
    }

    .\[\&\>a\]\:text-gray-13 > a {
        --tw-text-opacity: 1;
        color: rgb(19 19 19/var(--tw-text-opacity))
    }

    .\[\&\>a\]\:text-white > a {
        --tw-text-opacity: 1;
        color: rgb(255 255 255/var(--tw-text-opacity))
    }

    .\[\&\>a\]\:text-black > a {
        --tw-text-opacity: 1;
        color: rgb(0 0 0/var(--tw-text-opacity))
    }

    .\[\&\>a\]\:underline > a {
        text-decoration-line: underline
    }

    .\[\&\>a\]\:shadow-underline-blurple > a {
        --tw-shadow: inset 0 -1px 0 0 #5200ff;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color)
    }

    .\[\&\>a\]\:shadow-underline-black > a, .\[\&\>a\]\:shadow-underline-blurple > a {
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .\[\&\>a\]\:shadow-underline-black > a {
        --tw-shadow: inset 0 -1px 0 0 #000;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color)
    }

    .\[\&\>a\]\:shadow-underline-blurple-1 > a {
        --tw-shadow: 0 1px 0 0 #5200ff;
        --tw-shadow-colored: 0 1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .\[\&\>a\]\:shadow-underline-gray-13 > a {
        --tw-shadow: inset 0 -1px 0 0 #131313;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color)
    }

    .\[\&\>a\]\:shadow-underline-gray-13 > a, .\[\&\>a\]\:shadow-underline-gray-63 > a {
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .\[\&\>a\]\:shadow-underline-gray-63 > a {
        --tw-shadow: inset 0 -1px 0 0 #636363;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color)
    }

    .dark .dark\:\[\&\>a\]\:text-gray-bd > a {
        --tw-text-opacity: 1;
        color: rgb(189 189 189/var(--tw-text-opacity))
    }

    .dark .dark\:\[\&\>a\]\:shadow-underline-franklin > a {
        --tw-shadow: inset 0 -1px 0 0 #3cffd0;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .dark\:\[\&\>a\]\:shadow-underline-white > a {
        --tw-shadow: inset 0 -1px 0 0 #fff;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .dark\:\[\&\>a\]\:shadow-underline-gray-63 > a {
        --tw-shadow: inset 0 -1px 0 0 #636363;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
    }

    .dark .dark\:\[\&\>a\]\:shadow-underline-gray > a {
        --tw-shadow: inset 0 -1px 0 0 #bdbdbd;
        --tw-shadow-colored: inset 0 -1px 0 0 var(--tw-shadow-color);
        box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow)
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

