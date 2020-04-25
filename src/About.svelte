<script>

    let aboutUsContent = [
        "Sherdana is a family office with exclusive focus on emerging markets",

        "Our consolidates existing assets that have been developed on the continent since 2009 together with know-how and network to unlock new opportunities",

        "Sherdana’s operational headquarters are in Lusaka, Zambia"
    ]

</script>

<style>
    p {
        font-size: 1.2rem;
    }
    .lower {
        font-style: italic;
    }

    .upper {
        text-transform: uppercase;
        margin-bottom: 10px;
    }

</style>

<p class="upper">about us</p>
{#each aboutUsContent as value}
    <p class="lower"> {value} </p>
{/each}