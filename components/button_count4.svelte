<script lang='ts'>
    import ValueField from "./value_field.svelte";
  
    export let start_count:number;
    export let buttons:Button[];

    interface Button{
        label: string,
        value: number
    }
  
    let curr_count = start_count;
  
    function handleButtonClick(button:Button) {
      if (button.label === "R") {
        curr_count = start_count;
      } else {
        curr_count += button.value;
      }
    }
  </script>
  
  <div class="container">
    <ValueField title="" value={curr_count}/>
    <div class="button-row">
      {#each buttons as button (button.label)}
        <div
          class="square-button"
          role="button"
          on:click={() => handleButtonClick(button)}
          on:keydown={e => {
            if (e.key === "Enter") {
              handleButtonClick(button);
            }
          }}
          tabindex="0"
        >
          {button.label}
        </div>
      {/each}
    </div>
  </div>
  

<style>
  .container {
    box-sizing: border-box;
    width: 100%;
    margin: 5%
  }

  .button-row {
    display: flex;
    justify-content: space-around;
    width: 100%;
  }

  .square-button {
    width: 20%;
    height: 100%;
    background-color: #996590;
    color: #9CE685;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
  }
</style>