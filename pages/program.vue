<template>
  <div>
    <Navlink />
    <div class="program-hero row-grid">
      <div class="container">
        <img src="../assets/img/showcase2.JPG" alt="" />
      </div>
    </div>
    <div class="schedule-all1 row-max-grid">
      <div class="container">
        <div class="sch-title">
          <h1>Schedule</h1>
          <div class="decor-box1"></div>
        </div>
        <Schedule />
      </div>
    </div>

    <div class="pro-gallery row-max-grid row-bottom-grid">
      <div class="container">
        <h1>Gallery</h1>
        <div class="gallery-wrapper row-grid">
          <div
            class="single-img row-grid"
            v-for="item in gallery"
            :key="item.id"
          >
            <img :src="require('@/assets/img/' + item.img + '')" alt="" />
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Schedule from "../components/Schedule.vue";
export default {
  data() {
    return {
      gallery: [
        {
          id: 1,
          img: "gal1.jpg",
        },
        {
          id: 2,
          img: "gal2.jpg",
        },
        {
          id: 3,
          img: "gal3.jpg",
        },
        {
          id: 4,
          img: "gal4.JPG",
        },
        {
          id: 5,
          img: "gal5.JPG",
        },
        {
          id: 6,
          img: "gal6.jpg",
        },
        {
          id: 7,
          img: "gal7.jpg",
        },
        {
          id: 8,
          img: "gal8.JPG",
        },
        {
          id: 9,
          img: "gal9.JPG",
        },
        {
          id: 10,
          img: "gal10.jpg",
        },
        {
          id: 11,
          img: "gal11.JPG",
        },
        {
          id: 12,
          img: "gal12.jpg",
        },
      ],
    };
  },
  mounted() {},
  components: { Schedule },
};
</script>
