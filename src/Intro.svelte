<script lang="ts">
    import FactBlock from "./FactBlock.svelte";
</script>

<div id="flex">
    <div id="intro">
        <h2>Hello everyone and welcome to my personal website</h2>
        <p>My friends call me "Arsen"</p>
    </div>
    <FactBlock />
</div>

<style>
    #flex {
        display: flex;
        flex-direction: column;
        height: 100%;
    }
    #intro {
        flex-grow: 1;
    }
</style>
