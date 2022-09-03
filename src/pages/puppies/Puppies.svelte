<script>
    import microgreens from '../microgreens/microgreens.json'
    // import dove1 from '/images/pages/puppies/parents/doveFerns1.jpg'
    import puppies from './puppies1.json'

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
            Schnauzer Puppies
        </div>
    </div>

    <div class="container-list">
        <!-- <div class='main-title'>
            The Parents
        </div> -->
        <div class='container-border'>
            <div class='container'>
                <div class="allBorder">
                    <img class="allPuppy" src='images/pages/puppies/all.jpg' alt='puppy'>
                </div>

                <!-- Image Div -->
                <div>
                    <div class="parentName">
                        Dove (mother)
                    </div>
                    <img class="pupImg" src='/images/pages/puppies/parents/doveFerns1.jpg' alt='Puppy'/>
                </div>
                <div>
                    <div class="parentName">
                        Duke (father)
                    </div>
                    <img class="pupImg" src='/images/pages/puppies/parents/duke2.jpg' alt='Puppy'/>
                </div>
                <div class='drop-info'>
                    <div class='eating'>
                        <div class='parentText'>
                            Arsement Farms has had a litter of 5 schnauzer puppies from our lovely Dove! Dove is a 13 lb liver-tan, miniature schnauzer. She is mega-coated and double-ticked (roaned), meaning the white areas on her coat has liver mixed into it, which creates for a very beautiful coat. She has a very sweet temperament and is a great momma!
                        </div>
                        <div class='parentText'>
                            The puppies were born on August 3rd, 2022 and were just over 4 weeks old during the posting of these pictures (we will try to update pictures fairly reguarly.) We are currently accepting deposits for puppies ($500), and the puppies will be available to take home at 8 weeks old, September 28th.
                        </div>
                        <div class="parentText">
                            Please contact 409-673-0734 if you have an interest in any of the puppies listed below. Currently all puppies are available!
                        </div>
                        <div class='parentText'>
                            The father of the puppies is Duke, an 11 lb black schnauzer with a very thick mega-coat. He has a small white patch on his chest
                        </div>
                        <div class='parentText'>
                            Both of the parents are fully AKC registered and given that both are mega-coated we expect all or most of the puppies to also have a mega-coat. Their tails have been docked, their dew claws have been removed, and we provide up to date shots for our puppies. 
                        </div>

                        <div class='parentText'>  
                            The mother has slightly faded but the father has had no fading, so we expect the puppies to either not fade or have minimal fading. Additionally, we expect the three liver puppies to fall within 10-13 lbs at maturity but both of our black puppies are looking to be borderline teacup/toy size, possibly 7-10 lbs.
                        </div>
                    </div>
                </div>    
            </div>
        </div>
    </div>

    <div class='container-list'>
        {#each puppies as puppy, index}
            <div class='container-border'>
                <div class='container'>
                    <!-- Image Div -->
                        <div>
                            <img class="pupImg" src={puppy.imgHand} alt='Puppy'/>
                        </div>
                        <div>
                            <img class="pupImg" src={puppy.imgHolding} alt='Puppy'/>
                        </div> 
                    <div class='drop-info'>
                        <div class='eating'>
                            <div class='eat'>
                                <div class='eat-title'>
                                    Color:
                                </div>
                                <div class='eat-description'>
                                    {puppy.color}
                                </div>
                            </div>

                            <div class='eat'>
                                <div class='eat-title'>
                                Gender:
                                </div>
                                <div class='eat-description'>
                                    {puppy.gender}
                                </div>
                            </div>
                            <div class='eat'>
                                <div class='eat-title'>
                                Coat:
                                </div>
                                <div class='eat-description'>
                                    {puppy.coat}
                                </div>
                            </div>
                            <div class='eat'>
                                <div class='eat-title'>
                                Pattern:
                                </div>
                                <div class='eat-description'>
                                    {puppy.pattern}
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
    .allBorder{
        width: 1250px;
        margin: 0 auto;
        border-radius: 5px;
    }
    .allPuppy{
        height: 510px;
        width: 720px;
        padding: 2rem;
    }
    .parentText{
        font-size: 1.25rem;
        line-height: 1.4rem;
        margin: 1.25rem auto;
        padding: 0 2rem;
    }
    .parentName{
        width: fit-content;
        margin: auto;
        font-size: 2.5rem;
        font-weight: 700;
        color: black;
        padding: 0.75rem;
        background-color: #926d55;
        margin-bottom: 1rem;
        border-radius: 5px;
    }
    .header{
        background-color: #6fadbf;
        font-size: 4rem;
        color: black;
        padding: 2rem 0;
        font-weight: 800;
    }
    .header-border{
        background-color: #97c7d5;
        height: 95px;
        padding-top: 1rem;
    }

    main{
        padding-bottom: 8rem;
        min-height: 100vh;
        background-color: white;
    }

    /* Elements */
    .pupImg{
        height: 450px;
        width: 450px;
        background-color: aliceblue;
        border-radius: 5px;
        object-fit: fill;
    }

    /* Classes */

    /* Intro */
    /* .main-title{
        font-size: 4rem;
        font-weight: 800;
        color: black;
        margin-bottom: 2rem;
        margin-top: 5rem;
    } */
    
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
        justify-content: space-evenly;
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
    .drop-info{
        width: 82%;
        background-color: #d1d1d1;
        padding: 0.5rem;
        text-align: left;
        margin-top: 1rem;
        border-radius: 5px;
    }

    /* Below 1250 view width */
    @media (max-width: 1250px) {
        .allPuppy{
            height: 60vw;
            width: 80vw;
            padding: 2rem;
        }
        /* Elements */
        .pupImg{
            height: 40vw;
            width: 40vw;
            margin-bottom: 10px;
        }
        .container-list{
            width: 100%;
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
            justify-content: space-around;
        }
        /* Styling for each individual microgreen row */
        .container-border{
            width: 90%;
            margin: 2rem 1rem;
            padding: 1rem 5px;
        }
        .container{
            padding: 0.5rem 5px;
            width: 95%;
        }

        /* Bullet Point Listing of Microgreen Specifics */
        .eat{
            width: 340px;
        }
        .eat-title{
            font-size: 1.25rem;
            font-weight: 600;
            padding: 0.25rem;
        }
        .eat-description{
            font-size: 1.15rem;
        }

        /* Dropdown Info */
        .drop-info{
            width: 90%;
            /* height: 20rem; */
            padding: 0rem;
            text-align: left;
        }
    }

    /* Below 1000 view width */
    @media (max-width: 1000px) {
        /* Paragraph Contents */
        /* .main-title{
            font-size: 3.5rem;
            margin-bottom: 2rem;
        } */
    }

    /* Below 600 view width */
    @media (max-width: 600px) {
        .pupImg{
            height: 80vw;
            width: 80vw;
        }
        .header{
            padding: 1rem 0;
        }
        .header-border{
            font-size: 2.25rem;
            height: 70px;
        }
        /* .main-title{
            font-size: 3rem;
            margin-bottom: 1.5rem;
        } */
        .container{
            width: 100%;
            /* margin: 0; */
        }
        .container-border{
            padding: 0;
            margin: 1rem 0;
        }
        .container-list{
            margin: 0;
            padding: 0;
        }
        .parentText{
            padding: 0 0.75rem;
        }
        .drop-info{
            width: 95%;
        }
        .eat-title{
            width: 25%;
        }
        .eat-description{
            width: 75%;
            padding: auto;
        }
    }
</style>