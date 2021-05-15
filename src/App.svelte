<script>
  import DataView from "./Comps/DataHolderView.svelte";
  import ReliabilityView from "./Comps/Reliability.svelte";
  import DataPresentation from "./Comps/HowIsDataPresented.svelte";
  import Sauce from "./Comps/Sauce.svelte";
  let active = 0;
  let comps = [DataView, ReliabilityView, DataPresentation, Sauce];
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
      <button
        class="navbarButton"
        type="button"
        on:click={() => {
          active = 2;
        }}
      >
        How Data is Presented
      </button>
    </div>
    <div>
      <button
        class="navbarButton"
        type="button"
        on:click={() => {
          active = 3;
        }}
      >
        Sources
      </button>
    </div>
  </div>
  <div id="body" class="body">
    <svelte:component this={comps[active]} />
  </div>
</main>

<style>
  .navbar > div {
    display: inline-block;
  }
</style>
