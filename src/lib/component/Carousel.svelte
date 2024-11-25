<script>
  import emblaCarouselSvelte from "embla-carousel-svelte";
  import Autoplay from "embla-carousel-autoplay";

  const options = { loop: true, speed: 25 };
  const plugins = [Autoplay({ delay: 5000, speed: 250 })];
  const items = [
    "https://picsum.photos/id/13/2500/1667",
    "https://picsum.photos/id/14/2500/1667",
    "https://picsum.photos/id/15/2500/1667",
    "https://picsum.photos/id/16/2500/1667",
    "https://picsum.photos/id/18/2500/1667",
  ];

  let emblaApi;

  async function onInit(evt) {
    emblaApi = evt.detail;
  }
</script>

<section class="self-stretch mt-[70px] bg-zinc-400">
  <div class="overflow-hidden" use:emblaCarouselSvelte={{ options, plugins }}>
    <div class="flex">
      {#each items as item, i}
        <div
          class="flex-none w-full min-w-0 h-[200px] sm:h-[300px] md:h-[400px] lg:h-[500px] !bg-cover"
          style="background: url({item}) center center no-repeat;"
        ></div>
      {/each}
    </div>
  </div>
</section>
