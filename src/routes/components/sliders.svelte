<script>
  import { Slider, Checkbox } from "smelte";
  import Code from "docs/Code.svelte";
  import sliders from "examples/sliders.txt";

  let value = 0;
  let value2 = 0;
  let disabled = false;
</script>

<div class="my-4">
  <Checkbox label="Disabled" bind:checked={disabled} />
</div>

<h6>Basic</h6>

<caption>Value: {value}</caption>

<Slider min="0" max="100" bind:value {disabled} />

<h6 class="mt-8">With steps</h6>

<caption>Value: {value2}</caption>

<Slider min="0" step="20" max="100" bind:value={value2} {disabled} />

<Code code={sliders} />