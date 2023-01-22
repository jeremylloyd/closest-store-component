<svelte:head>
  <title>Stores Component</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    button, input {
      font-family: inherit;
      border-radius: 0;
      border: none;
    }
  </style>
</svelte:head>

<script>
  import ClosestStores from '$lib/components/ClosestStores.svelte';
</script>

<div class="page">
  <div class="container-store">
    <div class="shadow"></div>
    <ClosestStores/>
  </div>
</div>

<style>
  .page {
    background-color: #120C36;
    min-height: 100vh;
    font-family: 'Mulish', sans-serif;
  }

  .shadow {
    background-image: linear-gradient(
      135deg,
      #FF57AE 0%,
      #A752D9 70%
    );
    border-radius: 0px 25px;
    width: 300px;
    height: 300px;
  }
</style>