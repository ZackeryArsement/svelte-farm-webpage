<script>
    let github = 'images/footer/github.png';
    let linkedIn = 'images/footer/linkedIn.png';
    let portfolio = 'images/footer/cv.png';
</script>

<main>
    <div class="credit">
        Like the webpage? I created it myself! Check out my Github, LinkedIn, and Portfolio!
    </div>

    <div class="credit">
        <a href="https://www.linkedin.com/in/zackery-arsement/" target="_blank"  rel="noreferrer">
            <img class='img' src={linkedIn} alt="LinkedIn Icon"/>
        </a>

        <a href="https://github.com/ZackeryArsement" target="_blank"  rel="noreferrer">
            <img class='img' src={github} alt="Github Icon"/>
        </a>

        <a href="https://zackeryarsement.github.io/react-portfolio/" target="_blank"  rel="noreferrer">
            <img class='img' src={portfolio} alt="Portfolio Icon"/>
        </a>
    </div>

    <div>
        <a href="https://www.flaticon.com/free-icons/garden" title="garden icons">Garden icons created by Freepik - Flaticon</a>
        <a href="https://www.flaticon.com/free-icons/sprout" title="sprout icons">Sprout icons created by cahiwak - Flaticon</a>
        <a href="https://www.flaticon.com/free-icons/pumpkin" title="pumpkin icons">Pumpkin icons created by Umeicon - Flaticon</a>
        <a href="https://www.flaticon.com/free-icons/mushroom" title="mushroom icons">Mushroom icons created by Freepik - Flaticon</a>
        <a href="https://www.flaticon.com/free-icons/garden" title="garden icons">Garden icons created by Freepik - Flaticon</a>
        <a href="https://www.flaticon.com/free-icons/question-mark" title="question mark icons">Question mark icons created by Freepik - Flaticon</a>
        <a href="https://www.flaticon.com/free-icons/arrow-left" title="arrow left icons">Arrow left icons created by pictogramer - Flaticon</a>
        <a href="https://www.flaticon.com/free-icons/next" title="next icons">Next icons created by Kiranshastry - Flaticon</a>
    </div>
</main>

<style>
    main{
        padding: 1.5rem;
        background-color: rgb(207, 207, 207);
    }

    .credit{
        font-size: 1.2rem;
        font-style: italic;
        padding: 1rem;
    }

    .img{
        width: 75px;
        margin: 0 2rem;
    }
</style>