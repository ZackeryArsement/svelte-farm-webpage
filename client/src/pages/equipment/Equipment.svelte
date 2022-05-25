<script>
    import microgreenEquipments from './microgreenEquipment.json'

</script>

<main>
    <div class='headers'>
        <div class='header'>
            Equipment
        </div>
        <!-- <div class='sub-headers'>
            <div>
                Microgreens
            </div>
            <div>
                Pumpkins
            </div>
            <div>
                Mushrooms
            </div>
        </div> -->
    </div>

    <div class='body'>
        {#each microgreenEquipments as equipmentType}
            <div>
                <div class="title">
                    {equipmentType[Object.keys(equipmentType)[1]]}
                </div>
            
                <div class="scroller">
                    {#each equipmentType[Object.keys(equipmentType)[0]] as equipment}
                        <div class="item bg-green">
                            <img src={equipment.image} alt={equipment.name}/>
            
                            <div>
                                <div class="item-name">{equipment.name}</div>
                                <div class="item-price">{equipment.price}</div>
                                <a href={equipment.link} target="_blank" class="item-link">Purchase Here!</a>
                            </div>
                        </div>
                    {/each}
                </div>
            </div>
        {/each}
    </div>   
</main>

<style>
    main{
        background-color: #414141;
        min-height: 100vh;
    }
    img{
        width: 325px;
        height: 325px;
    }
    .scroller {
        display: flex;
        height: 475px;
        overflow: auto;
        white-space: nowrap;
        scrollbar-width: auto;
        scrollbar-color: black;
    }
    .body{
        width: 1500px;
        margin: auto;
        padding-bottom: 10rem;
    }

    /* Header stylings */
    .headers{
        margin-bottom: 4rem;
    }
    .header{
        background-color: black;
        font-size: 4rem;
        font-weight: 800;
        padding-top: 2rem;
        padding-bottom: 2rem;
        color: #cdcdcd;
    }
    /* .sub-headers{
        background-color: #1a1a1a;
        margin: auto;
        display: flex;
        font-size: 3rem;
        padding-top: 1rem;
        padding-bottom: 1rem;
        color: #cdcdcd;
        justify-content: space-around;
    } */

    /* Title */
    .title{
        color: white;
        text-align: left;
        margin: 6rem 0 1rem 0;
        padding-left: 25px;
        padding-bottom: 1rem;
        font-size: 5rem;
        border-bottom: 6px solid black;
    }

    /* Item styling */
    .item{
        padding: 1rem;
        margin: 0.5rem;
    }
    .item-name{
        color: white;
        font-size: 1.25rem;
        margin-top: 0.5rem;
    }
    .item-price{
        color: #333232;
        font-size: 1.33rem;
        font-weight: 600;
        padding: 0.5rem;
    }
    .item-link{
        color: #333232;
        font-size: 1.33rem;
        padding: 0.5rem;
        text-decoration: none;
    }
    .bg-green{
        background-color: #41874a;
    }
</style>