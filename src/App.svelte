<script lang="ts">
	import Signup from './../views/signup.svelte';
	import BidViewer from './../components/bid_viewer.svelte';
	import LoginView from './../views/login_view.svelte';
	import { navbarData } from './../resources/linkUtil.js';
  import Navbar from '../components/navbar.svelte';
  import CircleButton from '../components/circle_button.svelte';
    import BidView from '../views/bid_view.svelte';

    interface item{
        content:string,
        quantity:string,
        region:string,
        date:string,
        start_value:number,
        current_value:number,
        minimal_bid:number,
    }

  const item_info:item = {
    content: "plastico",
    quantity: "30R$",
    region: "Salvador - BA",
    date:  "10/07/5032",
    start_value: 10,
    current_value: 18,
    minimal_bid: 2
  }
</script>

  <Navbar data={navbarData}></Navbar>

<main>
  <div class="background">
    <div class="page_container">
      <div class="content">
        <BidView></BidView>
      </div>
    </div>
  </div>
  
</main>

<style>
  .background{
    position:fixed;
    padding:0;
    margin:0;

    top:0;
    left:0;

    width: 100%;
    height: 100%;
    background:#84FF5E;
    max-height: 100%;
  }
  .page_container{
    max-height: 100%;
    width: 100%;
    overflow-y: auto;
  }
  .content{
    margin-top: 7%;
  }
</style>
