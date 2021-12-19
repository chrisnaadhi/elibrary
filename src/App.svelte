<script>
  import NavBar from "./components/NavBar.svelte";
  import Hero from "./components/HeroLogin.svelte";
  import Layanan from "./components/Layanan.svelte";

  // Route
  import Member from "./pages/Member.svelte";
  import Profil from "./pages/Profil.svelte";
  import Koleksi from "./pages/Koleksi.svelte";
  import Panduan from "./pages/Panduan.svelte";

  let menu = "beranda";

  function handleMenu(e) {
    menu = e.detail.menu;
    console.log(menu);
  }
</script>

<main class="has-text-centered">
  <NavBar on:nav={handleMenu} />
  {#if menu === "beranda"}
    <Hero />
    <Layanan />
  {:else if menu === "member"}
    <Member />
  {:else if menu === "panduan"}
    <Panduan />
  {:else if menu === "profil"}
    <Profil />
  {:else if menu === "koleksi"}
    <Koleksi />
  {/if}
</main>

<style>
</style>
