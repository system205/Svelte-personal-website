<script lang="ts">
    import { createEventDispatcher } from "svelte";

    export let text: string;
    const a = () => {
        console.log("Clicked");
    };

    const dispatch = createEventDispatcher<{ page: string }>();
    function changePage(page: string) {
        dispatch("page", page);
    }
</script>

<header>
    <h1>{text}</h1>
    <nav>
        <button class="menu-item" on:click={() => changePage("Intro")}
            >Intro</button
        >
        <button class="menu-item" on:click={() => changePage("About")}
            >About</button
        >
    </nav>
</header>

<style>
    h1 {
        margin: 0;
        padding: 5px;
    }
    header {
        text-align: center;
        border-bottom: 3px solid #1b2631;
        border-radius: 0 0 15px 15px;
        background: linear-gradient(35deg, #1b2631, #aeb6bf, #ebedef);
    }
    .menu-item {
        border-style: inset;
        border-width: 2px;
        border-radius: 5px;
        transition-duration: 0.3s;
        height: 100%;
        background-color: #85929e;
    }
    .menu-item:focus {
        text-shadow: 0 0 5px #aeb6bf;
    }

    nav {
        height: 40px;
        padding: 3px;
    }
</style>
