<script>
    let keyboard = [
        { pressed: false, value: "+" },
        { pressed: false, value: "-" },
        { pressed: false, value: "X" },
        { pressed: false, value: "/" }
    ];


    function handleClick(index) {
        keyboard[index]["pressed"] = true;

        setTimeout(() => {
            keyboard[index]["pressed"] = false;
        }, 300);
    }
</script>

<div id="keyboard">
    {#each keyboard as key, index}
        <div
            on:click={() => handleClick(index)}
            class={key["pressed"] ? "pressed" : ""}
        >
            {key["value"]}
        </div>
    {/each}
</div>

<style lang="scss">
    #keyboard {
        display: inline-grid;

        grid-template-columns: 150px 150px ;
        grid-template-rows: 150px 150px;

        align-items: center;

        background-color: rgba(26, 35, 55, 0.656);

        div {
            display: flex;

            margin: 10px;

            width: 80%;
            height: 80%;

            background-color: rgba(17, 36, 71, 0.654);
            color: white;
            font-size: 4rem;

            border: thin black solid;
            justify-content: center;
            align-items: center;

            transition: transform 0.1s;

            &.pressed {
                transform: scale(0.95);
            }
            -webkit-user-select: none; /* Safari */
            -ms-user-select: none; /* IE 10 and IE 11 */
            user-select: none; /* Standard syntax */
        }
    }
</style>
