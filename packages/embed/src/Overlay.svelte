<svelte:options customElement="ysws-ring-overlay" />

<script lang="ts">
  import styles from "./styles.css?inline";
  import "@fontsource-variable/archivo";

  import { ArrowLeftIcon, ArrowRightIcon, ListIcon } from "@lucide/svelte";

  import flower1 from "./assets/flower1.svg";

  // https://stackoverflow.com/a/79718503/22946386
  const container = $host();
  const style = document.createElement("style");
  style.textContent = styles;
  container.shadowRoot?.appendChild(style);
</script>

<div class="border-border fixed top-6 left-6 w-72 border-2 bg-white shadow-md">
  <div class="flex h-10 items-center justify-between px-1">
    <button
      class="group grid size-8 place-items-center transition hover:bg-neutral-200"
    >
      <img src={flower1} alt="" class="h-5" />
      <span class="sr-only">Hide</span>
    </button>
    <button
      class="group grid size-8 place-items-center transition hover:bg-neutral-200"
    >
      <ArrowLeftIcon
        strokeWidth={2.5}
        class="size-4 transition not-group-hover:text-neutral-600"
      />
      <span class="sr-only">Previous website</span>
    </button>
    <p class="">
      <strong>page</strong> by Hack Club
    </p>
    <button
      class="group grid size-8 place-items-center transition hover:bg-neutral-200"
    >
      <ArrowRightIcon
        strokeWidth={2.5}
        class="size-4 transition not-group-hover:text-neutral-600"
      />
      <span class="sr-only">Next website</span>
    </button>
    <button
      class="group grid size-8 place-items-center transition hover:bg-neutral-200"
    >
      <ListIcon
        strokeWidth={2.5}
        class="size-4 transition not-group-hover:text-neutral-600"
      />
      <span class="sr-only">Hide</span>
    </button>
  </div>
  <p class="text-link p-2">Hello from app!</p>
</div>

<style>
</style>
