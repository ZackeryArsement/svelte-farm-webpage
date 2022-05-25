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
    <div class='header'>
        <div class='header-border'>
            Microgreens
        </div>
    </div>

    <div class='intro-container'>
        <div class='intro'>
            What are Microgreens?
        </div>
        <div class='paragraph'>
            In the most general sense microgreens are young seedlings of vegetables, herbs, and other edible plants. A typical microgreen is only grown for about 10 days after planting, hence the name 'micro'-greens due to their limited growth. Not to be confused with sprouts, microgreens are grown in soil and under lighting, while a sprout is grown in the absence of both. This allows for microgreens to be far less likely to have any mold or fungal growth upon harvest, while still allowing for the same benefits that sprouts provide at an early harvest.
        </div>
        <div class='description-list'>
            Harvesting after little growth has two major benefits:
            <ul>
                <li>Minimal Bitter Flavor</li>
                <li>More Concentrated Nutrients</li>
            </ul>
        </div>
        <div class='paragraph'>
            Since microgreens are harvested so young, the plant is low in chlorophyll concentrations and is therefore low in bitterness. This makes microgreens perfect for any dish that goes well with fresh greens, such as salads, sandwhiches, eggs, etc. The longer you grow the microgreen, the more bitter your sprout becomes! Typically you would like to harvest any microgreen as soon as its first 'true leaves' emerge from the plant.
        </div>
        <div class='paragraph'>
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

    <div class='container-list'>
        <div class='main-title'>
            Our Microgreens
        </div>
        {#each microgreens as microgreen, index}
            <div class='container-border'>
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
            </div>
        {/each}
    </div>
</main>

<style>
    .header{
        background-color: #41874a;
        font-size: 4rem;
        color: black;
        padding: 2rem 0;
        font-weight: 800;
    }
    .header-border{
        background-color: #5ab867;
        height: 95px;
        padding-top: 1rem;
    }
    main{
        padding-bottom: 8rem;
        background-color: white;
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
        margin-bottom: 4rem;
        width: 1000px;
        border-radius: 5px;
    }
    .main-title{
        font-size: 4rem;
        font-weight: 800;
        color: black;
        margin-bottom: 2rem;
    }

    /* Microgreen Containers */
    .container-list{
        width: 1300px;
        border-radius: 5px;
        margin: auto;
        padding: 1rem 0;
    }
    .description-list{
        text-align: left;
        margin: 1.5rem auto;
        padding: 0 1rem;
        font-size: 1.5rem;
        font-weight: 650;
        line-height: 1.70rem;
    }
    .description-list ul{
        margin-left: 200px;
        margin-top: 1rem;
        font-weight: 500;
        font-size: 1.5rem;
    }
    .intro{
        margin-top: 4rem;
        font-size: 3rem;
        font-weight: 500;
        text-align: left;
    }
    .paragraph{
        margin-top: 1rem;
        font-size: 1.5rem;
        text-align: left;
        line-height: 2rem;
    }

    
    /* Styling for each individual microgreen row */
    .container-border{
        background-color: #433934;
        border-radius: 5px;
        width: 1250px;
        margin: 2rem auto;
        padding: 1rem 0;
    }
    .container{
        background-color: #70523f;
        display: flex;
        flex-wrap: wrap;
        padding: 0.5rem;
        margin: auto;
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