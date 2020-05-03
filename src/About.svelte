<script>

    let aboutUsContent = [
        "Sherdana is a family office with exclusive focus on emerging markets",

        "Our approach consolidates existing assets that have been developed on the continent since 2009 together with know-how and network to unlock new opportunities",

        "Sherdana’s operational headquarters are in Lusaka, Zambia"
    ]

</script>

<style>

    p {
        font-size: 1.2rem;
        color: #1A2F21;

    }
    .lower {
        font-size: 1rem;
        margin: 5px 5px;
        color: #1A2F21;
        font-style: italic;
    }

    .upper {
        text-transform: uppercase;
        margin-bottom: 8px;
    }

    @media only screen and (min-width: 768px) {
        p {
            font-size: 2rem;
        }
        .lower {
            /*font-weight: lighter;*/
            font-size: 1.2rem;
            margin: 0px 0px 8px;
            width: 750px;
        }
    }


</style>

<p class="upper">about us</p>
<br />
{#each aboutUsContent as value}
    <p class="lower"> {value} </p>
{/each}