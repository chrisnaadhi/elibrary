<script>
  import { Swiper, SwiperSlide } from "swiper/svelte";
  import "swiper/css";

  const images = [
    { src: "./../images/1.jpg" },
    { src: "./../images/2.jpg" },
    { src: "./../images/3.jpg" },
    { src: "./../images/4.jpg" },
  ];
</script>

<div class="area mt-5 container">
  <h1 class="is-size-3 has-text-weight-medium">Layanan e-Resources</h1>
  <hr />
  <Swiper spaceBetween={50} slidesPerView={3}>
    {#each images as image}
      <SwiperSlide>
        <figure class="image is-1by1 mb-15">
          <img src={image.src} alt="E-Resources" />
        </figure>
      </SwiperSlide>
    {/each}
  </Swiper>
  <h1 class="is-size-2">Drag to preview</h1>
</div>

<style>
  hr {
    color: red;
    margin: 10px 255px;
  }

  figure {
    cursor: grab;
  }
</style>
