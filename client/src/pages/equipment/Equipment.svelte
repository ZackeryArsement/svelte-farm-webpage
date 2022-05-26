<script>
    import microgreenEquipments from './microgreenEquipment.json'

</script>

<main>
    <div class='headers'>
        <div class='header'>
            <div class='header-border'>
                Equipment
            </div>
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
        background-color: #8b8b8b;
        min-height: 100vh;
    }
    img{
        width: 350px;
        height: 350px;
    }
    .scroller {
        display: flex;
        height: auto;
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
        background-color: #736557;
        font-size: 4rem;
        color: #aea79f;
        padding: 2rem 0;
        font-weight: 800;
    }
    .header-border{
        background-color: black;
        height: 95px;
        padding-top: 1rem;
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

    @media (max-width: 1500px) {
        .body{
            width: 100%;
        }
        .title{
            margin: 6rem 0 1rem 0;
            padding-left: 2%;
            font-size: 4rem;
            width: 98%;
            border-bottom: 6px solid black;
        }
    }

    /* Below 600 view width */
    @media (max-width: 600px) {
        .item{
            padding: 1rem;
            margin: 0.5rem;
            height: 450px;
        }
        .item-name{
            width: 350px;
            white-space: normal;
        }
        .header{
            padding: 1rem 0;
        }
        .header-border{
            font-size: 3rem;
            height: 70px;
        }
    }
    /* Below 600 view width */
    @media (max-width: 450px) {
        .title{
            font-size: 3.25rem;
        }
    }
</style>