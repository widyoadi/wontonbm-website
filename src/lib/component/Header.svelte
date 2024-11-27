<script>
  import { goto } from "$app/navigation";
</script>

<!-- svelte-ignore a11y_click_events_have_key_events -->
<!-- svelte-ignore a11y_no_noninteractive_element_interactions -->
<header
  class="flex justify-center items-center self-stretch px-12 py-3 bg-white h-[70px] shadow-lg w-full fixed top-0 left-0 z-[1000]"
>
  <button class="m-0 h3 text-red-700 italic" on:click={() => goto("/")}>
  <img src="../images/logo_wonton.png" alt="Wonton BM">
  </button>
</header>
