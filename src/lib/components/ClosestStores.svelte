<script>
  import Store from '$lib/components/Store.svelte';
  import InputLocation from '$lib/components/InputLocation.svelte';

  let stores = [
    {
      "id": 0,
      "name": 'POINT Bergen Sentrum',
      "address": "Strandagaten 55-57, 6007 Bergen",
      "openHour": 9,
      "openMinute": 0,
      "closeHour": 19,
      "closeMinute": 0,
    },
    {
      "id": 1,
      "name": 'POIVestkanten',
      "address": "Strandagaten 55-57, 6007 Bergen",
      "openHour": 9,
      "openMinute": 0,
      "closeHour": 21,
      "closeMinute": 0,
    }
  ]
</script>

<article class='closest-stores'>
  <h2>Closest stores</h2>
  <InputLocation></InputLocation>
  <section class="container-stores">
    {#each stores as store}
      <Store storeData={store}></Store>
    {/each}
  </section>
  <button class="view-all">View all</button>
</article>

<style>
  .closest-stores {
    color: #C4B7EC;
    background: #0A061D;
    background: white;
    max-width: 25rem;
    padding: 30px;

    display: flex;
    flex-direction: column;
    gap: 30px;
  }

  .container-stores {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .view-all {
    color: white;
    background: #8253FD;
    padding: 10px;
  }
</style>