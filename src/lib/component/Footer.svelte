<script>
  import { Instagram, Phone } from "lucide-svelte";

  async function openMedia(media) {
    switch (media) {
      case "WhatsApp":
        window.open("https://wa.me/62881022748339", "_blank");
        break;
      default:
        window.open("https://www.instagram.com/wonton.bm/", "_blank");
        break;
    }
  }
</script>

<!-- svelte-ignore a11y_consider_explicit_label -->
<footer
  class="flex flex-col justify-start items-center self-stretch py-12 bg-red-700 text-red-100"
>
  <div class="flex items-end gap-6 px-12 max-w-screen-xl w-full">
    <div class="flex flex-col gap-1">
      <h2 class="h3 mb-3 text-white">Wonton BM</h2>
      <p>Jl. Cijawura Hilir no. 59B RT 01 RW 11</p>
      <p>Buahbatu, Kota Bandung, Jawa Barat 40287</p>
    </div>
    <div class="flex gap-3 ms-auto">
      <button
        class="inline-block"
        title="Hubungi kami via WhatsApp"
        on:click={() => openMedia("WhatsApp")}
      >
        <Phone size={36} />
      </button>
      <button
        class="inline-block"
        title="Kunjungi Instagram Wonton BM"
        on:click={() => openMedia("Instagram")}
      >
        <Instagram size={36} />
      </button>
    </div>
  </div>
</footer>
