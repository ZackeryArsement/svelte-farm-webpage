<script>
    // let Sunflowers = 'images/pages/microgreens/sunflowers.png'
    let Sprouts = 'images/navbar/sprout.png'

    import microgreens from './microgreens.json'

    let dropDownNutrition = [];
    let dropDownGrowing = [];

    for(let i=0; i<microgreens.length; i++){
        dropDownNutrition[i] = false;
        dropDownGrowing[i] = false;
    }
</script>

<main>
    <div class='intro-container'>
        <div class='intro-container-inner'>
            <div class='main-title'>
                What are Microgreens?
            </div>
            <div class='intro-description'>
                In the most general sense microgreens are young seedlings of vegetables, herbs, and other edible plants. A typical microgreen is only grown for about 10 days after planting, hence the name 'micro'-greens due to their limited growth. Not to be confused with sprouts, microgreens are grown in soil and under lighting, while a sprout is grown in the absence of both. This allows for microgreens to be far less likely to have any mold or fungal growth upon harvest, while still allowing for the same benefits that sprouts provide at an early harvest.
            </div>
            <div class='description-list'>
                Harvesting after little growth has two major benefits:
                <ul>
                    <li>No Bitter Flavor</li>
                    <li>More Concentrated Nutrients</li>
                </ul>
            </div>
            <div class='intro-description'>
                Since microgreens are harvested so young, the plant is low in chlorophyll concentrations and is therefore low in bitterness. This makes microgreens perfect for any dish that goes well with fresh greens, such as salads, sandwhiches, eggs, etc. The longer you grow the microgreen, the more bitter your sprout becomes! Typically you would like to harvest any microgreen as soon as its first 'true leaves' emerge from the plant.
            </div>
            <div class='intro-description'>
                In addition to their great flavor, microgreens boast an impressive resume when it comes to health benefits. Since microgreens are harvested so young they have all the energy from their seed condensed into the plant. Essentially microgreens are harvested at the optimal time in terms of nutrients because the plant has not started using its energy to grow into a fully mature plant. Once the green starts working towards maturing, the energy density of the plant becomes less compact. A study done by the Journal of Agricultural and Food Chemistry back in 2012 found that microgreens contain on average 4-6 times more nutrients than their adult counterparts and in the case of red cabbage microgreens 40 times more vitamin E was found.
            </div>
            <div class='description-list'>
                Additional Resources:
                <ul>
                    <li>
                        <a href="https://integrisok.com/resources/on-your-health/2021/july/what-are-microgreens" target="_blank">Integris Health</a>
                    </li>
                    <li>
                    <a href="https://totalgardener.com/why-microgreens-taste-bitter/" target="_blank">Total Gardener</a>
                    </li>
                </ul>
            </div>
        </div>

    </div>

    <div class='container-list'>
        <div class='main-title'>
            Our Microgreens
        </div>
        {#each microgreens as microgreen, index}
            <div class='container'>
                <!-- Image Div -->
                <div>
                    <img src={microgreen.img} alt='Sprout'/>
                </div>

                <!-- Content Div -->
                <div class='content'>
                    <div class='title'>
                        {microgreen.name}
                    </div>

                    <div class='body'>
                        <div class='description'>
                            {microgreen.description}
                        </div>

                        <div class='eating'>
                            <div class='eat'>
                                <div class='eat-title'>
                                    Flavor:
                                </div>
                                <div class='eat-description'>
                                    {microgreen.flavor}
                                </div>
                            </div>

                            <div class='eat'>
                                <div class='eat-title'>
                                   Texture:
                                </div>
                                <div class='eat-description'>
                                    {microgreen.texture}
                                </div>
                            </div>

                            <div class='eat'>
                                <div class='eat-title'>
                                    Est. Longevity:
                                </div>
                                <div class='eat-description'>
                                    {microgreen.longevity}
                                </div>
                            </div>

                            <a href={microgreen.infoLink} target="_blank">Further Information</a>
                        </div>
                    </div>

                </div>

                <!-- Drop Down Div -->
                <div class='button-list'>
                    <!-- Nutritional Facts -->
                    <div>
                        <button class='button-drop' on:click={() => dropDownNutrition[index] = !dropDownNutrition[index]}>Nutritional Facts</button>
                        <div class='drop-info' style={dropDownNutrition[index] ? 'display: block;' : 'display: none;'}>
                            <div class='eating'>
                                <div class='eat'>
                                    <div class='eat-title'>
                                        Vitamins:
                                    </div>
                                    <div class='eat-description'>
                                        {microgreen.vitamins}
                                    </div>
                                </div>
    
                                <div class='eat'>
                                    <div class='eat-title'>
                                       Essential Metals:
                                    </div>
                                    <div class='eat-description'>
                                        {microgreen.metals}
                                    </div>
                                </div>
    
                                <div class='eat'>
                                    <div class='eat-title'>
                                        Additional:
                                    </div>
                                    <div class='eat-description'>
                                        <ul>
                                            {#each microgreen.extras as extra}
                                                <li>
                                                    {#if extra.slice(0,5) === 'https'}
                                                        <a href={extra.split(' ')[0]} target='_blank'>{extra.split(' ')[1]}</a>
                                                    {:else}
                                                        {extra}
                                                    {/if}
                                                </li>
                                            {/each}
                                        </ul>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!-- Growing Facts -->
                    <div>
                        <button  class='button-drop' on:click={() => dropDownGrowing[index] = !dropDownGrowing[index]}>Growing Facts</button>
                        <div class='drop-info' style={dropDownGrowing[index] ? 'display: block;' : 'display: none;'}>
                            <div class='eating'>
                                <div class='eat'>
                                    <div class='eat-title'>
                                        Soak Seeds:
                                    </div>
                                    <div class='eat-description'>
                                        {microgreen.soak}
                                    </div>
                                </div>
    
                                <div class='eat'>
                                    <div class='eat-title'>
                                       Germination:
                                    </div>
                                    <div class='eat-description'>
                                        {microgreen.germination}
                                    </div>
                                </div>
    
                                <div class='eat'>
                                    <div class='eat-title'>
                                        Under Lights / Sun:
                                    </div>
                                    <div class='eat-description'>
                                        {microgreen.growing}
                                    </div>
                                </div>

                                <div class='eat'>
                                    <div class='eat-title'>
                                        Seed Density:
                                    </div>
                                    <div class='eat-description'>
                                        {microgreen.seedDensity}/tray
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        {/each}
    </div>
</main>

<style>
    main{
        padding: 8rem 0;
        background-color: #dbc49b;
        background-image: url('/images/backgrounds/cartographer.png');
        /* https://transparenttextures.com/ */
    }
    /* Elements */
    img{
        height: 450px;
        width: 450px;
        background-color: aliceblue;
    }
    li{
        margin-left: 25px;
        list-style: circle;
        line-height: 2rem;
    }

    /* Classes */

    /* Intro */
    .intro-container{
        padding: 1rem;
        margin: auto;
        margin-bottom: 10rem;
        width: 1500px;
        background-color: #433934;
        border-radius: 5px;
    }
    .intro-container-inner{
        background-color: #9c897c;
        color: black;
        padding: 1rem;
    }
    .main-title{
        font-size: 4rem;
        font-weight: 800;
        color: black;
        margin-bottom: 2rem;
    }
    /*  */
    .container-list{
        background-color: #433934;
        width: 1500px;
        border-radius: 5px;
        margin: auto;
        padding: 1rem;
    }
    .intro-description{
        text-align: left;
        margin-top: 1.5rem;
        padding: 0 1rem;
        font-size: 1.2rem;
        line-height: 1.70rem;
    }
    .description-list{
        text-align: left;
        margin: 1.5rem auto;
        padding: 0 1rem;
        font-size: 1.33rem;
        font-weight: 600;
        line-height: 1.70rem;
    }
    .description-list ul{
        margin-left: 200px;
        margin-top: 1rem;
        font-weight: 400;
        font-size: 1.2rem;
    }

    
    /* Styling for each individual micrgoreen row */
    .container{
        background-color: #70523f;
        display: flex;
        flex-wrap: wrap;
        margin: 3rem auto;
        padding: 0.5rem;
        width: 1200px;
    }
    .content{
        display: flex;
        flex-direction: column;
        width: 720px;
        padding: 0.5rem;
        background-color: #eaeaea;
        margin-left: 10px;
    }
    .body{
        display: flex;
        flex-direction: column;
        height: 360px;
        /* background-color: #70523f; */
    }
    .description{
        text-align: left;
        padding: 0 1rem;
        font-size: 1.2rem;
        line-height: 1.70rem;
    }
    .title{
        padding: 1rem;
        font-size: 2.5rem;
        font-weight: 700;
        text-decoration: underline
    }

    /* Bullet Point Listing of Microgreen Specifics */
    .eating{
        margin-top: auto;
        margin-bottom: 1rem;
    }
    .eat{
        /* background-color: #70523f; */
        display: flex;
        justify-content: center;
        margin: auto;
        width: 700px;
    }
    .eat-title{
        font-size: 1.5rem;
        font-weight: 700;
        width: 33%;
        text-align: right;
        padding: 0.5rem;
    }
    .eat-description{
        font-size: 1.25rem;
        width: 66%;
        padding: 0.5rem;
    }

    /* Dropdown Info */
    .button-list{
        width: 100%;
        margin: 1rem auto;
        padding: 0.5rem;
    }
    .button-drop{
        width: 100%;
        margin: 0 auto;
        padding: 0.5rem;
        font-size: 2rem;
        font-weight: 500;
        border-radius: 0;
    }
    .drop-info{
        background-color: #d1d1d1;
        padding: 0.5rem;
        text-align: left;
    }

</style>