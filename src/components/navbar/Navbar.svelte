<script>
    import { Router, Link } from "svelte-navigator"

    let leftArrow = true
    let CurrentArrow = leftArrow ? 'images/navbar/left-arrow.png' : 'images/navbar/right-arrow.png'

    let HomeIcon = 'images/navbar/home.png'
    let SproutIcon = 'images/navbar/sprout.png'
    let PumpkinIcon = 'images/navbar/pumpkin.png'
    let MushroomIcon = 'images/navbar/mushroom.png'
    let PuppyIcon = 'images/navbar/dog.png'
    let ToolsIcon = 'images/navbar/tools.png'
    let QuestionIcon = 'images/navbar/question.png'

    let IconArray = [
        {
            ref: HomeIcon,
            link: "/",
            alt: "Home Icon",
            bg: "#724a1b",
            brd: "#ae7a3f"
        },
        {
            ref: SproutIcon,
            link: "/microgreens",
            alt: "Sprout Icon",
            bg: "#41874a",
            brd: "#5ab867"
        },
        // {
        //     ref: PumpkinIcon,
        //     link: "/pumpkins",
        //     alt: "Pumpkin Icon",
        //     bg: "#e79111",
        //     brd: "#ffbc57"
        // },
        // {
        //     ref: MushroomIcon,
        //     link: "/mushrooms",
        //     alt: "Mushroom Icon",
        //     bg: "#d4ed94",
        //     brd: "#aac272"
        // },
        {
            ref: ToolsIcon,
            link: "/equipment",
            alt: "Tools Icon",
            bg: "#736557",
            brd: "#aea79f"
        },
        {
            ref: PuppyIcon,
            link: "/puppies",
            alt: "Puppy Icon",
            bg: "#6fadbf",
            brd: "#97c7d5"
        },
        {
            ref: QuestionIcon,
            link: "/questions",
            alt: "Question Icon",
            bg: "#b1aeac",
            brd: "#676767"
        },
    ]

    const clickArrow = () => {
        leftArrow = !leftArrow;
        CurrentArrow = leftArrow ? 'images/navbar/left-arrow.png' : 'images/navbar/right-arrow.png'
    }

</script>

<main>
    <div class='navbar' style={leftArrow ? 'display: block; visibility:visible' : 'display: none; visibility: none'}>
            <Router>
                {#each IconArray as icon}
                    <div class='img-border' style={`background-color: ${icon.brd}`}>
                        <Link to={icon.link}>
                            <img src={icon.ref} alt={icon.alt} style={`background-color: ${icon.bg}`} class="navImg"/>
                        </Link>
                    </div>
                {/each}
            </Router>
    </div>
    <div class="arrowButton">
        <button on:click={() => clickArrow()}>
            <img class='arrow' src={CurrentArrow} alt='arrow-symbol' />
        </button>
    </div>
</main>

<style>
    main{
        display: flex;
        width: 190px;
        position: fixed;
		top: 50%;
        left: 0;
        transform: translate(0, -50%);
    }

    button{
        position: relative;
        top: 50%;
        transform: translate(0, -50%);
        translate: 50%;
        background-color: #aea79f;
        border-top-right-radius: 5px;
        border-bottom-right-radius: 5px;
        text-align: center;
        margin-left: -16px;
    }

    .navImg{
        height: 96px;
        width: 96px;
        border-radius: 15px;
        margin: 6px auto;
        padding: 8px;
    }

    .navbar{
        display: block;
        width: 160px;
        background-color: #807047;
        border-top-right-radius: 10px;
        border-bottom-right-radius: 10px;
        box-shadow: 3px 5px 5px #888888;
    }

    .img-border{
        margin: 1rem auto;
        border-radius: 15px;
        width: 124px;
        height: 124px;
    }

    .arrow{
        padding: 0;
        width: 15px;
        height: 30px;
        margin-left: 0;
    }

    /* Below 600 view width */
    @media (max-width: 600px) {
        main{
            width: 115px;
        }

        .navImg{
            height: 48px;
            width: 48px;
            border-radius: 7px;
            margin: 4px auto;
            padding: 8px;
        }

        .navbar{
            width: 90px;
            box-shadow: 2px 2px 2px #888888;
        }

        .img-border{
            margin: 0.5rem auto;
            border-radius: 7px;
            width: 72px;
            height: 72px;
        }

        .arrow{
            width: 10px;
            height: 20px;
        }
	}
</style>
