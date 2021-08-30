<script lang="ts">
    //const lucky: string = "https://www.youtube.com/watch?v=dQw4w9WgXcQ";
    let luck: boolean = false;

    // async function getDoujin(id: string) {
    //     let url: string = "https://nhentai.net/g/" + id + "/";
    //     const response: Response = await fetch(url, { mode: "no-cors" });
    //     console.log(response);
    // }

    function getLucky() {
        //window.location.replace(lucky);
        luck = true;
    }

    //getDoujin("177013");
</script>

<main>
    <h1>Hello Gaymrs!</h1>
    <h2>This website is made for Nathan</h2>
    {#if luck}
        <iframe
            width="560"
            height="315"
            src="https://www.youtube.com/embed/dQw4w9WgXcQ?autoplay=1"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
        />
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

    @media (min-width: 640px) {
        main {
            max-width: none;
        }
    }
</style>
