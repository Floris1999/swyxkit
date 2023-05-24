<script>
    import image1 from '$lib/assets/surfing.jpg';
    import image2 from '$lib/assets/guitar.jpg';
    import image3 from '$lib/assets/maroc.jpg';

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

<div class="carousel h-full w-full ">
    <img class="carousel-image object-cover h-full w-full" src={images[currentImageIndex]} alt={`Image ${currentImageIndex}`} />

    <div class=" h-14 w-full flex justify-end">

        <button
                class="block bg-orange-600 px-5 py-3 text-center text-xs font-bold uppercase text-gray-900 transition hover:bg-yellow-400 rotate-180"
                on:click={previousImage}
        >
            <svg role="img" height="16" width="16" aria-hidden="true" viewBox="0 0 16 16"
                 data-encore-id="icon" class="Svg-sc-ytk21e-0 eNWijz">
                <path d="M7.19 1A.749.749 0 0 1 8.47.47L16 7.99l-7.53 7.521a.75.75 0 0 1-1.234-.815.75.75 0 0 1 .174-.243l5.72-5.714H.75a.75.75 0 1 1 0-1.498h12.38L7.41 1.529a.749.749 0 0 1-.22-.53z"></path>
            </svg>
        </button>

        <button
                class="block bg-orange-600 px-5 py-3 text-center text-xs font-bold uppercase text-gray-900 transition hover:bg-yellow-400"
                on:click={nextImage}
        >
            <svg role="img" height="16" width="16" aria-hidden="true" viewBox="0 0 16 16"
                 data-encore-id="icon" class="Svg-sc-ytk21e-0 eNWijz">
                <path d="M7.19 1A.749.749 0 0 1 8.47.47L16 7.99l-7.53 7.521a.75.75 0 0 1-1.234-.815.75.75 0 0 1 .174-.243l5.72-5.714H.75a.75.75 0 1 1 0-1.498h12.38L7.41 1.529a.749.749 0 0 1-.22-.53z"></path>
            </svg>
        </button>
    </div>
</div>

<style>
    .carousel {
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .carousel-image {
        max-width: 100%;
        max-height: 100%;
    }
</style>
