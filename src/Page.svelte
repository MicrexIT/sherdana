<style>
    section {
        background-color: #E5E5E5;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: auto;
    }

    p {
        font-style: italic;
    }

    h1 {
        font-size: 4.5rem;
        font-weight: bold;
        letter-spacing: 8px;
    }
</style>

<script>
    import {pageNumber} from "./store"
    import About from "./About.svelte"
    import Contact from "./Contact.svelte"

    let currentPage

    const unsubscribe = pageNumber.subscribe(value => {
        currentPage = value
    })


</script>

<section>
    <section class="page cols">
        {#if currentPage == 1}
          <About/>

        {:else if currentPage === 2}
          <Contact/>
        {:else}
        <h1>
            SHERDANA
        </h1>
        <p>
            Family office
        </p>
        {/if}
    </section>
</section>
