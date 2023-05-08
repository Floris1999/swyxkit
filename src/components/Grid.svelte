<script>
    import { onMount } from 'svelte';

    function randomColor() {
        return '#' + Math.floor(Math.random() * 16777215).toString(16);
    }

    let columns = 0;
    let rows = 0;
    let total = 1;

    function getGridSize() {
        columns = Math.floor(document.body.clientWidth / 50);
        rows = Math.floor(document.body.clientHeight / 50);
        total = rows * columns;
    }

    onMount(() => {
        getGridSize();
        window.addEventListener('resize', getGridSize);
    });
</script>

<div class="container">
    <div id="grid">
        {#each Array(total) as _, i}
            <div class="grid-item" />
        {/each}
    </div>
</div>

<style>
    .container {
        background: var(--bg-color);
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    #grid {
        width: 400px;
        height: 500px;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(50px, 1fr));
        grid-template-rows: repeat(auto-fit, minmax(50px, 1fr));
        justify-content: center;
    }

    .grid-item {
        min-width: 100%;
        min-height: 100%;
        background-color: white;
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
