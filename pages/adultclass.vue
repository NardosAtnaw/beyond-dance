<template>
  <div>
    <Navlink />

    <div class="events row-grid">
      <div class="separt2 row-grid">
        <div class="container">
          <h1>Adults Classes</h1>
          <!-- <img
            class="wed-img1 row-grid row-bottom-grid"
            src="../assets/img/events/yoga.webp"
            alt=""
          /> -->
          <div class="box"></div>
        </div>
      </div>
      <div class="container">
        <div class="wedding-event">
          <div class="wrapper">
            <div class="wed-offer">
              <h2>Yoga</h2>
            </div>
            <div class="small-offer">
              <div class="single-offer1">
                <img src="../assets/img/events/YogaFlyer.jpg" alt="" />

                <p></p>
              </div>
              <div class="single-offer1">
                <img src="../assets/img/events/yoga.webp" alt="" />

                <p></p>
              </div>
            </div>
          </div>
        </div>
        <div class="separt2 row-grid">
          <div class="container">
            <div class="box"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="cta-register row-max-grid">
      <div class="container">
        <h1>Book Now</h1>
        <div class="separt-line"></div>
        <img src="../assets/img/events/yoga.webp" alt="" />
        <p>
          Join Us Today! If you are interested in joining Beyond Dance Studio,
          events and classes contact us to secure your spot with us!
        </p>
        <button class="btn btn-thrid">
          <nuxt-link to="/contactus">Book Now </nuxt-link>
        </button>
      </div>
    </div>
    <Contactus />
    <Footer />
  </div>
</template>

<script>
export default {
  mounted() {},
};
</script>
