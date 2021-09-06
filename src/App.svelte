<script lang="ts">
    let luck: boolean = false;

    function getLucky() {
        luck = true;
    }
</script>

<main>
    <h1>Hello Gaymrs!</h1>
    <h2>This website is made for Nathan</h2>
    {#if luck}
        <div id="CursedContainer">
            <a href="https://nhentai.net/g/177013/" target="_blank">
                <div id="UnholyBox" /></a
            >
            <iframe
                id="RickAstley"
                src="https://www.youtube.com/embed/dQw4w9WgXcQ?autoplay=1"
                title="YouTube video player"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
            />
        </div>
        <h2>
            Hello Comrade, You can't stop this Rick Roll.<br />
            Trust me, <span class="red">DON'T CLICK IT.</span> You've been warned.
        </h2>
    {:else}
        <button on:click={getLucky}>Click Here</button>
    {/if}
</main>

<style>
    main {
        text-align: center;
        padding: 1em;
        max-width: 240px;
        margin: 0 auto;
    }

    h1 {
        color: #ff3e00;
        text-transform: uppercase;
        font-size: 4em;
        font-weight: 100;
    }

    #CursedContainer,
    #UnholyBox,
    #RickAstley {
        height: 315px;
        width: 560px;
    }

    #CursedContainer {
        margin: 0 auto;
    }

    #UnholyBox {
        margin: 0 auto;
        float: left;
        /*background-color: rgba(255, 0, 0, 0.5);*/
        position: absolute;
    }

    #RickAstley {
        margin: 0 auto;
        float: left;
    }

    span.red {
        color: red;
    }

    @media (min-width: 640px) {
        main {
            max-width: none;
        }
    }
</style>
