<script>
  import DataView from "./Comps/DataView.svelte";
  import ReliabilityView from "./Comps/Reliability.svelte";
  let active = 0;
  let comps = [DataView, ReliabilityView];
</script>

<main>
  <div id="navbar" class="navbar">
    <div>
      <button
        class="navbarButton"
        type="button"
        on:click={() => {
          active = 0;
        }}
      >
        Data
      </button>
    </div>
    <div>
      <button
        class="navbarButton"
        type="button"
        on:click={() => {
          active = 1;
        }}
      >
        Reliability
      </button>
    </div>
    <div>
      <button class="navbarButton" type="button" on:click>
        PlaceHolder
      </button>
    </div>
    <div>
      <button class="navbarButton" type="button" on:click>
        PlaceHolder
      </button>
    </div>
  </div>
  <div id="body" class="body">
    {active}
    <svelte:component this={comps[active]} />
  </div>
</main>

<style></style>
