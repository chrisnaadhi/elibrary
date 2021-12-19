<script>
  import HeroBox from "./../components/HeroBox.svelte";
</script>

<HeroBox>
  <h1 class="is-size-5 has-text-weight-medium has-text-right">
    Selamat Datang, Chrisna!
  </h1>
</HeroBox>

<HeroBox>
  <div class="is-flex-direction-row pt-5">
    <div class="columns">
      <div class="column">
        <figure class="image">
          <img
            src="https://i.pinimg.com/236x/21/61/81/216181366c759c7aed39b462b72d30ee.jpg"
            alt=""
          />
        </figure>
      </div>
      <div class="column has-text-left">
        <p>Nama : Chrisna Adhi Pranoto</p>
        <p>NPM : 1234567</p>
        <p>Jurusan : Ilmu Perpustakaan</p>
      </div>
    </div>
    <div class="buttons is-flex is-justify-content-center">
      <button class="button is-primary">Peminjaman</button>
      <button class="button is-info">Pengembalian</button>
      <button class="button is-danger">Logout</button>
    </div>
  </div>
</HeroBox>

<style>
  .image {
    border: 3px solid orange;
  }

  .buttons {
    margin-bottom: 15px;
  }

  .button {
    margin: 5px;
  }
</style>
