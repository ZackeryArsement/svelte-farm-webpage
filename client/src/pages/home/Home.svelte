<script>
    import { Router, Link } from "svelte-navigator"

    let jumbotron = 'images/pages/home/jumbotron.jpg';
    let logo = 'images/pages/home/arsementFarmLogo.png';
</script>

<main>
    <div class='header'>
        <div class='header-border'>
            <img class="logo" src={logo} alt="Home"/>
        </div>
    </div>

    <div class='content'>
        <div>
            <img  class="jumbotron" src={jumbotron} alt="Home"/>
        </div>

        <div class='intro'>
            Welcome to the Farm!
        </div>

        <div class='paragraph'>
            We are a small local farm from Kountze, Texas that specializes in microgreens! Currently we only supply microgreens through the Beaumont Farmers Market, which is open every <b class="bold">Saturday from 8AM-11AM</b>, located at <b class="bold"><a href="https://www.google.com/maps/place/Beaumont+Farmers+Market/@30.0671471,-94.1703095,18z/data=!4m5!3m4!1s0x863ecc9500865969:0xa66a1d8e8d943660!8m2!3d30.0672655!4d-94.1693251" target="_blank">6525 College St. Beaumont, TX</a></b>.
        </div>
        <div class='intro'>
            Our Mission
        </div>
        <div class='paragraph'>
            Our number one goal and hope for Arsement Farms is to introduce the community to a product that many may be unfamiliar with. Interacting with individuals at the farmers market, it has become evident that many people don't know about the healthy goodness of microgreens! Check out our <Router><Link to='/microgreens'><b class="bold">microgreen</b></Link></Router> page to learn more!
        </div>
        <div class='paragraph'>
            Our farm strives for transparency and we would love to help others on their journey to becoming growers themselves! Because of this, all equipment used and seeds we buy will be listed on our website! Check out our <Router><Link to='/equipment'><b class="bold">equipment</b></Link></Router> page to learn more!
        </div>
        <div class='intro'>
            Future Goals
        </div>
        <div class='paragraph'>
            Although we currently specialize solely in microgreens, we have plans to expand into other areas of untouched health niches of our local food market. As these plans come closer to fruition we will be sharing additional information on these market adventures!
        </div>
        <div class='paragraph bold'>
            Please Join us in our Growth as a Supplier of Healthy Foods!
        </div>

        <div class='intro'>
            Contact Information
        </div>
        <div class='paragraph'>
            If you have any questions or concerns please contact us via email: <a href = "mailto: arsementfarms@gmail.com">arsementfarms@gmail.com</a>
        </div>
        <div class='paragraph italics'>
            We do sell and deliver if you would like to purchase in bulk on a reoccuring schedule or for any special event. However, due to the grow time of our microgreens we will need a 14 day (2 week) notice for any special order. Please email me for further information!
        </div>

        <div class='intro'>
            Donations
        </div>
        <div class='paragraph'>
            Has any of our information helped you on your journey to become your own grower? Please feel free to donate to the farm!
        </div>
    </div>
</main>

<style>
    main{
        background-color: white;
        min-height: 100vh;
    }
    .logo{
        height: 160px;
        object-fit: cover;
        margin-top: -15px;
    }
    .header{
        background-color: #3c220d;
        padding: 2rem 0;
    }
    .header-border{
        background-color: #654429;
        height: 110px;
        /* padding-bottom: 0.5rem; */
    }
    .jumbotron{
        width: 1000px;
    }

    /* Paragraph Contents */
    .content{
        width: 1000px;
        margin: auto;
        margin-bottom: 10rem;
    }
    .intro{
        margin-top: 2rem;
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
    .bold{
        font-weight: 600;
    }
    .italics{
        font-style: italic;
    }
</style>