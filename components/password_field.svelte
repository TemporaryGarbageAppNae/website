<script lang="ts">
    export let hint:string;

    let show_password = false;
    $: type = show_password ? "text" : "password";

    let see_password = '../resources/dont_see_password_icon.png'
    let dont_see_password = '../resources/see_password_icon.png'
</script>

<div style="position: relative;">
    <input type={type} id={$$props.id} placeholder={hint}>
    <button class="show_password_button" type="button" id='show_password' 
                    on:click={() => show_password = !show_password}>
        <img src={show_password ? see_password : dont_see_password} alt="buttonpng" />
        </button>

</div>

<style>
    input{
        width: 100%;
        height: 100%;
        padding: 12px 55px 12px 20px;
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
    .show_password_button {
        position: absolute;
        right: 15px;
        top: 40%;
        background-color: transparent;
        transform: translateY(-50%);
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0;
        border: none;
    }
    
    .show_password_button:hover{
        outline: none;
    }

    .show_password_button:focus{
        outline: none;
    }
</style>


