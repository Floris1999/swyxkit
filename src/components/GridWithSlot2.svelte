<script>
    import {onMount} from 'svelte';

    export let height;
    let columns = 0;
    let rows = 0;
    let total = 1;

    function getGridSize() {
        columns = Math.floor(document.body.clientWidth / 50);
        rows = Math.floor(height / 50);
        total = rows * columns;
    }

    onMount(() => {
        getGridSize();
        window.addEventListener('resize', getGridSize);
    });
</script>

<div id="grid" style="height: {height}px">
    <slot></slot>
    {#each Array(total) as _, i}
        <div class="grid-item"></div>
    {/each}
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
        outline: 1px solid black;
        display: block;
    }

    .grid-item:hover {
        opacity: 0.8;
    }
</style>
