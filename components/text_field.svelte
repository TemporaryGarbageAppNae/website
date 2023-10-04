<script lang=ts>
    export let hint:string;
</script>

<style>
    input{
        width: 100%;
        height: 100%;
        padding: 12px 20px;
        margin: 8px 0;
        display: inline-block;
        border: 6px solid #9CE685;
        background-color: white;
        color: black;
        font-size: 30px;
        border-radius: 60px;
        box-sizing: border-box;
        margin-bottom: 30px;
    }
</style>
<div>
    <input type="text" id={$$props.id} placeholder={hint}>
</div>