<script lang="ts">
  import {onMount} from 'svelte';
  import Card from './Card.svelte';

  interface Viso{
    event_title: string;
    id: number;
    event_type: string;
  }
  

  const fetchData = async () =>{
    try {
      const response = await fetch('https://nord.is/bakendi/feed/');


      const jsonData = await response.json();
      console.log(jsonData.feed);
      return jsonData.feed;
    }
    catch (error){
      console.log('Error fetching data: ', error);

      throw(error)
    }
    
  }

  let visoData: Promise<Viso[]> = fetchData()
  
</script>

<main>
  <div id="viso-container">
    {#await visoData}
      <p>loading...</p>
    {:then data}
      {#each data as item}
        {#if item.event_type === 'Vísó'}
        <Card event_title = {item.event_title}/>
          
        {/if} 
      {/each}
    {:catch error}
          <p>Error fetching data: {error.message}</p>
        
    {/await}
  </div>
</main>

<style>
  *{
  display: flex;
  align-items: center;
}

  #viso-container{
  display: grid;
  width: 100%;
}

  
</style>
