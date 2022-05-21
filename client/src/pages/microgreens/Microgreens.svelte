<script>
    // import Sunflowers from '../../../public/images/pages/microgreens/sunflowers.png'

    let microgreens = [
        {
            name: "Sunflowers",
            img: "images/pages/microgreens/sunflowers.png",
            description: "My Favorite! :P",
            taste: "Nutty",
            texture: "Crunchy",
            soak: "Yes; 12 hrs minimum",
            vitamins: "A, B Complex, C, D, E, K",
            metals: "Copper, Iron, Calcium, Magnesium and more!",
            extras: [
                "Lecithin: Clears arteries of deposits",
                "Essential Amino Acids"
            ],
            link: "https://homemicrogreens.com/sunflower-microgreens-nutrition/"
        },
        {
            name: "Sweet Peas",
            img: "images/pages/microgreens/sweetpeas.png",
            description: "Taste exactly like sweet peas",
            taste: "Pea Flavor; Sweet",
            texture: "Fibery",
            soak: "Yes; 6 hrs minimum",
            vitamins: "A, C",
            metals: "Iron, Calcium",
            extras: [
                "Protein",
                "Phytoestrogens: Helps lower the risk of cancer and heart disease"
            ],
            link: "https://www.longislandmicrogreens.com/blogs/news/pea-microgreens-fight-disease-cancer-and-promote-good-health?fbclid=IwAR29aWXr3fHRU6bJ9JM2IG9qIK58r4W_HgaPRjlWW5a8jNC6JlVUI8Aq3u0"
        },
        {
            name: "Radish",
            img: "images/pages/microgreens/radish.png",
            description: "Spicy boi, but nice in salad",
            taste: "Spicy/Peppery",
            texture: "Crunchy",
            soak: "No",
            vitamins: "A, B Complex, C, E",
            metals: "Manganese, Magnesium, Phosphorus and more!",
            extras: [
                "Antioxidants",
                "Essential Amino Acids"
            ],
            link: "https://homemicrogreens.com/radish-microgreen-nutrition/"
        },
        {
            name: "Broccoli",
            img: "images/pages/microgreens/broccoli.png",
            description: "Super healthy!",
            taste: "Strong Broccoli; (some say slightly bitter/peppery...)",
            texture: "Slightly Crunch",
            soak: "No",
            vitamins: "A, B, C, E, K",
            metals: "Iron, Zinc, Magnesium and more!",
            extras: [
                "Sulforaphane: Too many benefits to list! Check link below!",
            ],
            link: "https://microgreensworld.com/broccoli-microgreens-nutrition/?fbclid=IwAR3wVNskSIdEbrUCMxw5XlgkovJCmQVYu8qjzNZBFEZ90nZkhLil8IKPHQ4"
        },
        {
            name: "Alfalfa",
            img: "images/pages/microgreens/alfalfa.png",
            description: "I like on sandwiches",
            taste: "Fresh & Green",
            texture: "Very Crunchy",
            soak: "No",
            vitamins: "C, K",
            metals: "Copper, Iron, Magnesium",
            extras: [
                "Helps improve metabolic health",
                "Antioxidants"
            ],
            link: "https://www.healthline.com/nutrition/alfalfa#other-benefits"
        },
        {
            name: "Basil",
            img: "images/pages/microgreens/basil.png",
            description: "Delicious, strong basil flavor!",
            taste: "Strong Basil; Slightly Licorice",
            texture: "Slight Crunch",
            soak: "No",
            vitamins: "A, C, K",
            metals: "Manganese, Magnesium, Calcium, Iron",
            extras: [
                "Omega-3 Fatty Acids",
                "Essential Amino Acids",
                "Antioxidants"
            ],
            link: "https://soakandsoil.com/basil-microgreens-how-to-grow-pests-benefits-faqs/"
        },
    ]

</script>

<main>
    <div>
        <h1>What are Microgreens?</h1>
        <div>
            <p>
                Description of microgreens and a lot of text...
            </p>
        </div>
    </div>

    <div>
        <h1>My Microgreens</h1>
        {#each microgreens as microgreen}
            <div>
                {microgreen.name}
            </div>
            
        {/each}
    </div>
</main>

<style>
    h1{
        padding: 1rem;
    }
</style>