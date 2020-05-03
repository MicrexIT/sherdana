<style>
    section {
        padding: 8px;

    }
    img {
        width: 232px;
    }

    .line {
        margin-top: 8px;
        background-color: #D3B68D;
        height: 2px;
        width: 100%;
        border-radius: 4px;
    }
    ul {
        display: flex;
        justify-content: center;
        margin-top:8px;
    }

    li {
        padding-left: 8px;
        padding-right: 8px;
        font-size: 1rem;
        font-weight: lighter;
        cursor: pointer;
        color: #D3B68D;
        text-transform: capitalize;

    }

    .selected {
        font-weight: bolder !important;
        color: #D3B68D;
    }

    @media only screen and (min-width: 768px) {
        section {
            padding: 20px 100px 10px;
        }
        img {
            width: 20%;
            min-width: 400px;
        }

        .line {
            margin-top: 10px;
        }
        ul {
            margin-top:10px;
        }

        li {
            padding-left: 10px;
            padding-right: 10px;
            font-size: 1.2rem;
        }

    }


</style>
<script>
    import {pageNumber} from './store'
    let navItems = [
        {label: "HOME"},
        {label: "ABOUT"},
        {label: "CONTACT"},
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
    <img src="logo.png" alt="Sherdana"/>
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