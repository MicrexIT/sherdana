<style>
    main {
        min-height: 100%;
        display: grid;
        grid-template-rows: 16rem minmax(14rem, auto) 14rem;
        grid-template-columns: 1fr;
    }
   @media only screen and (min-width: 768px) {
       main {
           min-height: 100%;
           grid-template-rows: 21rem minmax(12rem,auto) 6.8rem;
           grid-template-columns: 1fr;
       }
   }

</style>


<script>
    import Footer from "./Footer.svelte"
    import Nav from "./Nav.svelte"
    import Page from "./Page.svelte"

    function spin(node, { duration }) {
        return {
            duration,
            css: t => ``
        };
    }

</script>
<main>
    <Nav/>
    <Page />
    <Footer/>
</main>
