<script lang='ts'>
    
    import offers from '../resources/offers.json'
    import BidViewer from '../components/bid_viewer.svelte';

    interface offer{
        id:string,
        content:string,
        quantity:string,
        region:string,
        date:string,
        start_value:number,
        current_value:number,
        minimal_bid:number,
    }
</script>

<div class="grid_container">
    {#each offers as offer (offer.id)}
      <BidViewer item_info={offer} />
    {/each}
</div>

<style>
    .grid_container {
    display: grid;
    grid-template-columns: repeat(2, auto); /* Adjust column width as needed */
    gap: 5%; /* Adjust gap between grid items */
  }
</style>