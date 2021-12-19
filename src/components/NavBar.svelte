<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  const navBarMenu = ["Beranda", "Profil", "Koleksi", "Panduan"];
</script>

<nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="container">
    <div class="navbar-brand">
      <a
        href="/"
        class="navbar-item"
        on:click|preventDefault={() => dispatch("nav", { menu: `beranda` })}
      >
        <img
          src="https://upload.wikimedia.org/wikipedia/id/thumb/8/80/Lambang_Universitas_Padjadjaran.svg/241px-Lambang_Universitas_Padjadjaran.svg.png"
          alt="Logo Unpad"
          class="image"
        />
        <p class="is-size-5 has-text-weight-medium">Universitas Padjadjaran</p>
      </a>

      <a
        href="/#"
        role="button"
        class="navbar-burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarBasic"
      >
        <span aria-hidden="true" />
        <span aria-hidden="true" />
        <span aria-hidden="true" />
      </a>
    </div>

    <div id="navbarMenu" class="navbar-menu">
      <div class="navbar-end">
        {#each navBarMenu as nav}
          <a
            href="/"
            class="navbar-item"
            on:click|preventDefault={() =>
              dispatch("nav", { menu: `${nav.toLowerCase()}` })}
          >
            {nav}
          </a>
        {/each}
        <div class="navbar-item">
          <div class="buttons">
            <button
              class="button is-primary"
              on:click|preventDefault={() =>
                dispatch("nav", { menu: "member" })}
            >
              Login
            </button>
            <button class="button is-primary is-outlined"> Register </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</nav>

<style>
  p {
    margin: 0 10px;
  }

  .navbar-end > a:hover {
    border-bottom: 1px solid black;
  }

  nav {
    box-shadow: 0 1px 8px 0 rgba(0, 0, 0, 0.2);
  }
</style>
