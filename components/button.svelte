<script lang=ts>
    export let message:string;
    export let method: () => void;
</script>

<style>
    input[type=submit] {
        width: 100%;
        height: 100%;
        background-color: #E65ECF;
        color: black;
        font-size: 30px;
        padding: 12px 20px;
        margin: 8px 0;
        text-align: center;
        border: 6px solid #9CE685;     
        border-radius: 60px;
        cursor: pointer;
        font-weight: bold;
    }

    input[type=submit]:hover{
        background-color: #e65ecfc5;
    }
</style>

<div>
    <input type="submit" id="button" on:click={method} value={message}>
</div>