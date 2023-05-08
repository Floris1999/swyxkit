<script>
    import {onMount} from 'svelte';

    export let height;
    let columns = 0;
    let rows = 0;
    let total = 1;

    function getGridSize() {
        columns = Math.floor(document.body.clientWidth / 50);
        rows = Math.floor(height / 50);

        console.log(columns)
        console.log(rows, height)
        total = rows * columns;
    }

    onMount(() => {
        getGridSize();
        window.addEventListener('resize', getGridSize);
    });
</script>

<div id="grid"
                 style="
                 height: {height}px;
                 background-image: linear-gradient(to right, #d9e2e9 1px, transparent 1px),linear-gradient(to bottom, #d9e2e9 1px, transparent 1px); background-size: 50px 50px">

    <slot></slot>
    <!--{#each Array(total) as _, i}-->
    <!--    <div class="grid-item outline outline-1 outline-black dark:outline-white"></div>-->
    <!--{/each}-->
</div>

<style>
    #grid {
        width: 100%;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(50px, 1fr));
        grid-template-rows: repeat(auto-fit, minmax(50px, 1fr));
        /*margin-bottom: 50px;*/
        /*justify-content: center;*/
    }

    .grid-item {
        min-width: 100%;
        min-height: 100%;
        /*background-color: white;*/
        cursor: pointer;
        position: relative;
    }

    .grid-item:after {
        content: '';
        position: absolute;
        width: 100%;
        height: 100%;
        left: 0;
        top: 0;
        /*outline: 1px solid;*/
        display: block;
    }

    .grid-item:hover {
        opacity: 0.8;
    }
</style>
