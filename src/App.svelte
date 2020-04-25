<style>

    /******** GLOBAL STYLES ***********/
    :global(html) {
        box-sizing: border-box;
        font-size: 16px;
        font-family: monserrat, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
        text-align: center;
    }

    :global(*, *:before, *:after) {
        box-sizing: inherit;
    }

    :global(body, h1, h2, h3, h4, h5, h6, p, ol, ul) {
        margin: 0;
        padding: 0;
        font-weight: normal;
    }

    :global(ol, ul) {
        list-style: none;
    }

    :global(img) {
        max-width: 100%;
        height: auto;
    }
    :global(a, a :visited, a :hover, a :active) {
    font-style: inherit;
    color: inherit;
    background-color: transparent;
    font-size: inherit;
    text-decoration: none;
    font-variant: inherit;
    font-weight: inherit;
    line-height: inherit;
    font-family: inherit;
    }

    /*********************************/
    main {
        min-height: 100%;
        display: grid;
        grid-template-rows: 30rem minmax(7.5rem,1fr) 6.8rem;
        grid-template-columns: 1fr;
    }

</style>


<script>
    import Footer from "./Footer.svelte"
    import Nav from "./Nav.svelte"
    import Page from "./Page.svelte"

</script>
<main>
    <Nav/>
    <Page/>
    <Footer/>
</main>
