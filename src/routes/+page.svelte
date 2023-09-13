<script>
    import Display from "./display.svelte";
    import NumKeyboard from "./numKeyboard.svelte";
    import OperationKeyboard from "./operationKeyboard.svelte";
</script>

<Display/>

<div id="keyboard">

    <NumKeyboard/>
<OperationKeyboard/>
</div>

<style>
    #keyboard{
        background-color: rgb(6, 6, 44);

        display: inline-flex;
        align-items: center;
        justify-content: center;

        padding: 15px;
        margin: 20px;
    }
</style>