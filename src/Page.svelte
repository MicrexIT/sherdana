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
        font-size: 1rem;
        letter-spacing: 3px;
        font-weight: lighter;
        color: #F5F2EA;

    }

    h1 {
        font-weight: bold;
        color: #F5F2EA;
        font-size: 3rem;
        letter-spacing: 6px;

    }

    @media only screen and (min-width: 768px) {
       p {
           font-size: 1.5rem;
           letter-spacing: 4px;
       }
       h1 {
           font-size: 4.5rem;
           letter-spacing: 8px;
        }
    }
</style>

<script>

    import {fade} from "svelte/transition"
    import {pageNumber} from "./store"
    import About from "./About.svelte"
    import Contact from "./Contact.svelte"

    let currentPage

    const unsubscribe = pageNumber.subscribe(value => {
        currentPage = value
    })


</script>

<section transition:fade class="page cols">
    {#if currentPage == 1}
        <About/>

    {:else if currentPage === 2}
        <Contact/>
    {:else}
        <h1>
            SHERDANA
        </h1>
        <p>
            LIMITED
        </p>
    {/if}
</section>
