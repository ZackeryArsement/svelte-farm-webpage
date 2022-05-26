<script>
    import { Route, Router } from "svelte-navigator";

    import Equipment from "../../pages/equipment/Equipment.svelte";
    import Home from "../../pages/home/home.svelte";
    import Microgreens from "../../pages/microgreens/Microgreens.svelte";
    import Mushrooms from "../../pages/mushrooms/Mushrooms.svelte";
    import Pumpkins from "../../pages/pumpkins/Pumpkins.svelte";
    import Questions from "../../pages/questions/Questions.svelte";
</script>

<Router>
    <main>
        <Route path='/'>
            <Home />
        </Route>
        <Route path='equipment'>
            <Equipment />
        </Route>
        <Route path='microgreens'>
            <Microgreens />
        </Route>
        <Route path='mushrooms'>
            <Mushrooms />
        </Route>
        <Route path='pumpkins'>
            <Pumpkins />
        </Route>
        <Route path='questions'>
            <Questions />
        </Route>
    </main>
</Router>


<style>
    main{
        min-height: 100vh;
        background-color: beige;
        position: relative;
        top: 0;
    }
</style>