<script>

</script>

<div class="location">
  <div class="container-input">
    <label class='location__label' for="postcode">Postal Code</label>
    <input class='location__input' type="text" id="postcode" placeholder="5055">
  </div>
  <button class="location__button">
    <span class="location__text">Use my location</span>
  </button>
</div>

<style>
  .location {
    display: flex;
  }

  .location__text {
    border: dashed 1px green;
  }

  .location__label {
    color: #C4B7EC;
  }

  .location__input {
    color: #C4B7EC;
    background: #0A061D;
    padding: 10px;
  }

  .location__button {
    display: flex;
    justify-content: space-between;
    align-items: center;

    flex-shrink: 0;

    color: #8253FD;
    background: transparent;

    border: dashed 1px orange;
  }
</style>