<script>
  import emblaCarouselSvelte from "embla-carousel-svelte";
  import Autoplay from "embla-carousel-autoplay";

  const options = { loop: true, speed: 25 };
  const plugins = [Autoplay({ delay: 5000, speed: 250 })];
  const items = [
    "images/200_78.png",
    "images/icetea.png",
    "images/Logo_mie_ayam_spanduk_miring copy.jpg",
    "images/WhatsApp Image 2024-11-17 at 20.38.50_dd14539a.jpg",
    "images/WhatsApp Image 2024-11-17 at 20.40.00_f969bb66.jpg",
    "images/Wonton_90_90.png",
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
