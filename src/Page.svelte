<style>
    section {
        background-color: #D3B68D;

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: auto;
    }

    p {
        font-size: 1.5rem;
        font-weight: thin;
        letter-spacing: 4px;
        color: #F5F2EA;

    }

    h1 {
        font-size: 4.5rem;
        font-weight: bold;
        letter-spacing: 8px;
        color: #F5F2EA;

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
            CAPITAL
        </p>
        {/if}
    </section>
</section>
