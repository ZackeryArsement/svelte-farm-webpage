<script>
    let thoughtBubble = 'images/pages/faq/question.png';
    import questions from './questions.json'
</script>

<main>
    <div class='icon'>
        <img src={thoughtBubble} alt='Thought Bubble'/>
        <div class='title'>
            FAQ
        </div>
    </div>


    <div class='content'>
        <div class='description'>
            {#each questions as question}
                <div class='intro'>
                    {question.question}
                </div>
                {#each question.answer as currentAnswer}
                    <div class='paragraph'>
                        {currentAnswer}
                    </div>
                {/each}
            {/each}
        </div>
    </div>
</main>

<style>
    main{
        background-color: white;
        min-height: 100vh;
    }
    img{
        width: 250px;
    }
    .icon{
        position: relative;
        background-color: #b1aeac;
    }
    .title{
        font-size: 4rem;
        color: black;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    /* Paragraph Contents */
    .content{
        width: 1000px;
        margin: auto;
        margin-bottom: 10rem;
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
    /* Below 1000 view width */
    @media (max-width: 1000px) {

        /* Paragraph Contents */
        .content{
            width: 600px;
            margin-bottom: 7rem;
        }
        .intro{
            font-size: 2.5rem;
        }
        .paragraph{
            font-size: 1.25rem;
            line-height: 1.5rem;
        }
	}

    /* Below 600 view width */
    @media (max-width: 600px) {
        /* img{
            width: 175px;
        } */
        /* .title{
            font-size: 3rem;
        } */
        /* Paragraph Contents */
        .content{
            width: 100%;
            margin: 0;
            margin-bottom: 3rem;
        }
        .description{
            padding: 1rem;
        }
	}
</style>