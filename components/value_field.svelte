<script lang='ts'>
    export let value:number;  
    export let title:string;
</script>

<div class=container>
    <div class="title">
        {#if title !== ""}
            {title}
        {/if}
    </div>
    <div class="field">
        {value}
    </div>
</div>

<style>
    *{
        box-sizing: border-box;
        max-width: 100%;
        flex: 1;
    }
    .title{
        text-align: left;
        color: black;
        padding-left: 0;
        font-size: 180%;
    }
    .field{
        color: #9CE685;
        width: 100%;
        height: 100%;
        padding: 5%;
        margin: 5% 0;
        display: inline-block;
        background-color: #996590;
        border-radius: 30px;
        font-size: 20px;
    }
</style>