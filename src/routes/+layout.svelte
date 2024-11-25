<script>
  import "../app.css";

  import Header from "$lib/component/Header.svelte";
  import Footer from "$lib/component/Footer.svelte";
</script>

<svelte:head>
  <title>
    {import.meta.env.VITE_APP_NAME}
  </title>

  <meta property="og:title" content={import.meta.env.VITE_APP_NAME} />
  <meta property="og:image" content="/favicon.png" />
</svelte:head>

<Header />
<slot />
<Footer />
