<template>
  <div>
    <Navlink />
    <!-- <Homevideo video="751212036" class="row-grid" /> -->
    <div class="container">
      <p class="row-grid"></p>
      <Aboutvideo video="751212036" class="video" />
    </div>

    <div class="show-case row-grid">
      <div class="container">
        <h4>Show Case and Performances of 2022</h4>
        <div class="show-videos row-grid">
          <div class="single-video">
            <iframe
              src="https://www.youtube.com/embed/uqEmLvvkg4k"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
          <div class="single-video">
            <iframe
              src="https://www.youtube.com/embed/hZsczpTkXj8"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
          <div class="single-video">
            <iframe
              src="https://www.youtube.com/embed/1G6uCoGnBRs"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
          <div class="single-video">
            <iframe
              src="https://www.youtube.com/embed/7bRxWXRofeM"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
        </div>
      </div>
    </div>
    <div class="cta-register row-max-grid">
      <div class="container">
        <h1>Register Now</h1>
        <div class="separt-line"></div>
        <img src="../assets/img/program/gal11.webp" alt="" />
        <p>
          Join Us Today! If you are interested in joining Beyond Dance Studio,
          we encourage you to pre-register to secure your spot with us!
        </p>
        <button class="btn btn-secondary">
          <nuxt-link to="/register">Register Now </nuxt-link>
        </button>
      </div>
    </div>
    <!-- <div class="big-image row-grid">
      <div class="container">
        <img src="../assets/img/gal11.JPG" alt="" />
      </div>
    </div> -->
    <Contactus />

    <Footer />
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  mounted() {},
};
</script>
