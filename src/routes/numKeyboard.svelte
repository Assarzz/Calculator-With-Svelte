<script>
    let keyboard = [];
    for (let index = 0; index < 10; index++) {
        keyboard[index] = { pressed: false, value: index };
    }

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

        grid-template-columns: 100px 100px 100px;
        grid-template-rows: 100px 100px 100px;

        align-items: center;

        background-color: rgba(36, 47, 70, 0.618);

        div {
            display: flex;

            margin: 10px;

            width: 80%;
            height: 80%;

            background-color: rgba(26, 51, 93, 0.668);
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
