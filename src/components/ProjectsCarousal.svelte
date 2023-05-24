<script>
    import {fly} from "svelte/transition";

    import image1 from '$lib/assets/surfing.jpg';
    import image2 from '$lib/assets/guitar.jpg';
    import image3 from '$lib/assets/maroc.jpg';
    import Carousel from "./Carousel.svelte";
    import hero from "$lib/assets/PXL_20220717_142943888.MP.jpg";

    let images = [
        image1,
        image2,
        image3,
    ];
    let currentImageIndex = 0;

    function nextImage() {
        currentImageIndex = (currentImageIndex + 1) % images.length;
    }

    function previousImage() {
        currentImageIndex = (currentImageIndex - 1 + images.length) % images.length;
    }
</script>

<section class="relative flex w-full items-center border-b border-black dark:border-gray-600">
    <div class="relative mx-auto w-full items-center 2xl:max-w-7xl">
        <div class="grid grid-cols-1 divide-y divide-black border-black md:grid-cols-4 md:divide-x md:divide-y-0 2xl:border-x dark:border-gray-600 h-full" >
            <div class="col-span-3 block w-full lg:mt-0 bg-orange-600 h-60">
                <img class="carousel-image object-cover h-full w-full" src={images[currentImageIndex]} alt={`Image ${currentImageIndex}`} />
            </div>

            <div class="bg-amber-50 relative items-center gap-12 p-8 lg:inline-flex lg:px-20 col-span-1">
                <p>Description</p>
            </div>

            <div class="col-span-3 block w-full lg:mt-0 ">
                <div class="flex">
                    <p class="mt-4 max-w-xl tracking-tight text-black dark:text-white xl:text-2xl">
                        React ab
                    </p>
                    <button>Read</button>
                </div>
            </div>

            <div class="w-full flex">
                <button
                        class="bg-orange-600  w-full text-gray-900 transition hover:bg-yellow-400 flex items-center justify-center rotate-180"
                        on:click={previousImage}
                >
                    <svg role="img" height="16" width="16" aria-hidden="true" viewBox="0 0 16 16"
                         data-encore-id="icon" class="Svg-sc-ytk21e-0 eNWijz">
                        <path d="M7.19 1A.749.749 0 0 1 8.47.47L16 7.99l-7.53 7.521a.75.75 0 0 1-1.234-.815.75.75 0 0 1 .174-.243l5.72-5.714H.75a.75.75 0 1 1 0-1.498h12.38L7.41 1.529a.749.749 0 0 1-.22-.53z"></path>
                    </svg>
                </button>

                <button
                        class="bg-orange-600 px-5 py-3 w-full text-gray-900 transition hover:bg-yellow-400 flex items-center justify-center"
                        on:click={nextImage}
                >
                    <svg role="img" height="16" width="16" aria-hidden="true" viewBox="0 0 16 16"
                         data-encore-id="icon" class="Svg-sc-ytk21e-0 eNWijz">
                        <path d="M7.19 1A.749.749 0 0 1 8.47.47L16 7.99l-7.53 7.521a.75.75 0 0 1-1.234-.815.75.75 0 0 1 .174-.243l5.72-5.714H.75a.75.75 0 1 1 0-1.498h12.38L7.41 1.529a.749.749 0 0 1-.22-.53z"></path>
                    </svg>
                </button>
            </div>
        </div>
    </div>
</section>
