<script lang='ts'>
	import CircleButton from './circle_button.svelte';
    import ButtonCount4 from "./button_count4.svelte";
    import ValueField from "./value_field.svelte";
    import {starting_bid_str, current_bid_str, min_bid_str, bid_button_str} from "../resources/strings.json"
    import bid_buttons from "../resources/bid_buttons.json"
    export let item_info:item;
    
    interface item{
        content:string,
        quantity:string,
        region:string,
        date:string,
        start_value:number,
        current_value:number,
        minimal_bid:number,
    }

    function bid(){

    }

</script>

<div class="container">
    <div class="top_row">
        <h2>{item_info.content}: {item_info.quantity}</h2>
        <h2>{item_info.region}</h2>
        <h3>{item_info.date}</h3>
    </div>
    <div class="row">
        <div class=column>
            <ValueField title={starting_bid_str} value={item_info.start_value}/>
            <ValueField title={current_bid_str} value={item_info.current_value}/>
            <ValueField title={min_bid_str} value={item_info.minimal_bid}/>
        </div>
        <div class=column>
            <div class="centered_column">
                <ButtonCount4 start_count={item_info.minimal_bid} buttons={bid_buttons}/>
                <CircleButton title={bid_button_str} method={() => bid}/>
            </div>
            
        </div>
    </div>
</div>

<style>
    .container{
        height: fit-content;
        margin: 5%;
        background-color: #9CE685;
        border-radius: 30px;
        width:fit-content;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .row{
        display: flex;
        flex-direction: row;
        padding: 1%;
        margin: 1% 2%;
        width: 100%;
    }
    .top_row{
        display: flex;
        flex-direction: row;
        align-items: center;
        padding: 1%;
        margin: 1% 2%;
        width: 500px;
    }
    h2{
        color: black;
        padding: 1% 2%;

    }
    h3{
        color:black;
        opacity: 50%;
        padding: 1% 2%;
    }
    .column{
        display: flex;
        flex-direction: column;
        align-items:stretch;
        margin: 1%; 
        width: 50%;
        height: 50%;
    }
    .centered_column{
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 13%;
    }
</style>