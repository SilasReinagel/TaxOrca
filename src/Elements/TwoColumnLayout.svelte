<script>
  import Container from './Container.svelte';
</script>

<Container>
  <div class="row">
    <div class="column">
      <slot name="first" />
    </div>
    <div class="column">
      <slot name="second" />
    </div>
  </div>
</Container>

<style>
  .row {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-evenly;
    margin: 1.5em 0 8em 0;
  }

  .column {
    max-width: 80vw;
    width: 640px;
    display: flex;
    flex-direction: column;
    margin: 0px 2em;
  }

  @media screen and (max-width: 600px) {
    .column {
      width: 100%;
    }
  }
</style>
