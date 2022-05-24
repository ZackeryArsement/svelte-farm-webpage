<script>
    import microgreenEquipments from './microgreenEquipment.json'

</script>

<main>
    <div class='header'>
        Equipment
    </div>


    <div class="scroller">
        {#each microgreenEquipments.traysAndShelves as equipment}
            <img src={equipment.image} alt={equipment.name}/>
        {/each}
    </div>

    <div class="scroller">
        {#each microgreenEquipments.miscellaneous as equipment}
            <img src={equipment.image} alt={equipment.name}/>
        {/each}
    </div>

    <div class="scroller">
        {#each microgreenEquipments.seeds as equipment}
            <img src={equipment.image} alt={equipment.name}/>
        {/each}
    </div>

    <div class="scroller">
        {#each microgreenEquipments.market as equipment}
            <img src={equipment.image} alt={equipment.name}/>
        {/each}
    </div>
</main>

<style>
    main{
        background-color: #414141;
        min-height: 100vh;
    }
    img{
        width: 300px;
        height: 300px;
    }
    .scroller {
        /* width: 1200px; */
        height: 350px;
        overflow: auto;
        white-space: nowrap;
        scrollbar-width: auto;
        scrollbar-color: black;
    }
    .header{
        background-color: black;
        font-size: 3rem;
        padding: 2rem;
        color: #cdcdcd;
    }
</style>