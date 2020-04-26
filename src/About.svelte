<script>

    let aboutUsContent = [
        "Sherdana is a family office with exclusive focus on emerging markets",

        "Our approach consolidates existing assets that have been developed on the continent since 2009 together with know-how and network to unlock new opportunities",

        "Sherdana’s operational headquarters are in Lusaka, Zambia"
    ]

</script>

<style>
    p {
        font-size: 2rem;
        color: #1A2F21;

    }
    .lower {
        font-size: 1rem;
        margin: 5px 0;
        color: #1A2F21;

    }

    .upper {
        text-transform: uppercase;
        margin-bottom: 10px;
    }

</style>

<p class="upper">about us</p>
<br />
{#each aboutUsContent as value}
    <p class="lower"> {value} </p>
{/each}