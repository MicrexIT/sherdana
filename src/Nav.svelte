<style>
    section {
        padding: 10px;

    }

    @media (min-width: 768px) {
        section {
            padding: 20px;
            padding-left: 100px;
            padding-right: 100px;
        }
    }


    img {
        width: 20%;
        min-width: 400px;
    }

    .line {
        background-color: #1D1D1B;
        height: 2px;
        width: 100%;
        border-radius: 4px;
    }
    ul {
        display: flex;
        justify-content: center;
        margin-top:10px;
    }

    li {
        /*font-family: "Comic Sans MS";*/
        padding-left: 10px;
        padding-right: 10px;
        font-weight: lighter !important;
        font-size: 1.2rem;
        cursor: pointer;

    }
    li :hover {
        opacity: 0.7;
    }
    .selected {
        /*opacity: 0.7;*/
    }


</style>
<script>
    import {pageNumber} from './store'
    let navItems = [
        {label: "home"},
        {label: "contacts"},
        {label: "about us"},
    ]
    let currentPage;

    function updatePageNumber(newNumber) {
        pageNumber.set(newNumber);
    }

    const unsubscribe = pageNumber.subscribe(value => {
        currentPage = value;
    });
</script>

<section>
    <img src="logo-black.png" alt="Sherdana"/>
    <div class="line"/>
    <ul>
        {#each navItems as item, index}
            {#if index==currentPage}
            <li class="selected">
               {item.label}
            </li>
            {:else}
                <li on:click={() => updatePageNumber(index)} >
                    {item.label}
                </li>
            {/if}
        {/each}
    </ul>

</section>