<script>
  import { time } from '$lib/stores.js';

  export let storeData;
  let open = (
    (
      $time.hour > storeData.openHour || (
        $time.hour === storeData.openHour
        && $time.minute >= storeData.openMinute
      )
    ) && (
      $time.hour < storeData.closeHour || (
        $time.hour === storeData.closeHour
        && $time.minute <= storeData.closeMinute
      )
    )
  );
</script>

<div class="store">
  <header class="store__header">
    <h3>{storeData.name}</h3>
    <span class="store__status" class:store__status--open={open} class:store__status--closed={!open}>{open ? 'Open' : 'Closed'}</span>
  </header>
  <p>{storeData.address}</p>
  <p>
    {storeData.openHour.toString().padStart(2, '0')}:{storeData.openMinute.toString().padStart(2, '0')} - {storeData.closeHour.toString().padStart(2, '0')}:{storeData.closeMinute.toString().padStart(2, '0')}
  </p>
</div>

<style>
  .store {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }

  .store__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .store__status {
    text-transform: uppercase;
    color: white;
    font-size: 0.8rem;
    padding: 3px 8px;
    border-radius: 1000px;
  }

  .store__status--open {
    background-color: #20BA94;
  }

  .store__status--closed {
    background-color: #F851A6;
  }
</style>