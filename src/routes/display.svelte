
<script>
    let displayEquation = "0"
</script>
<div>
    <h1>{displayEquation}</h1>
</div>

<style lang="scss">

    :global(body){
        background-color: #080842;
        opacity: 0.8;
        background-image:  repeating-radial-gradient( circle at 0 0, transparent 0, #11113f 10px ), repeating-linear-gradient( #444cf755, #444cf7 );
    }
    div{
        display: flex;
        background-color: rgba(0, 0, 0, 0.748);
        width: 100%;
        height: 100px;
        border: thick rgb(1, 84, 143) solid;
        border-radius: 40px;
        align-items: center;

        
        h1{
            display: flex;
            color: white ;
            margin-left: 50px;
            margin-right: 50px;
            font-size: 5rem;

            align-items: center;
            
        }
    }
</style>