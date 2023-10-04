<script lang='ts'>
    export let title:string;
    export let method: () => void;
</script>

<button type="button" on:click={method}>
    {title}
</button>


<style>
    button{
        margin: 5%;
        width: 160px;
        height: 160px;
        background-color: #E65ECF;
        border: 6px solid #84FF5E;
        border-radius: 50%;
        font-size: 16px;
        text-align: center;
        color: #9CE685;
    }
</style>

