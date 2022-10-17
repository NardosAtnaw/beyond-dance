<template>
  <div>
    <Navlink />
    <!-- <Homevideo video="744993912" class="row-grid" />
    -->
    <div class="events row-grid">
      <div class="separt2 row-grid">
        <div class="container">
          <h1>Events</h1>
          <div class="box"></div>
        </div>
      </div>
      <div class="container">
        <div class="wedding-event">
          <div class="wrapper">
            <div class="wed-offer"></div>
            <div class="big-offer">
              <div class="one-offer" v-for="items in events" :key="items.id">
                <div>
                  <img
                    :src="require('@/assets/img/' + items.eventimg + '')"
                    alt=""
                  />
                </div>
                <div>
                  <h4>{{ items.eventtitle }}</h4>
                  <p>{{ items.eventdesc }}</p>
                  <button class="btn btn-thrid">
                    <nuxt-link to="items.url">{{ items.link }}</nuxt-link>
                  </button>
                </div>
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
        <img src="../assets/img/events/coporate.webp" alt="" />
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
  data() {
    return {
      events: [
        {
          id: 1,
          eventtitle: "Kids Event",
          eventdesc: "Celebrate your Birthday Party with fun and Dance!",
          eventimg: "program/gal6.webp",
          url: "/kidsevent",
          link: "Kids Event",
        },

        {
          id: 6,
          eventtitle: "Wedding Packages",
          eventdesc: "Celebrate your special event with a Dancing & Fun!",
          eventimg: "events/slowdance.webp",
          url: "/wedding",
          link: "Wedding Packages",
        },
        {
          id: 4,
          eventtitle: "Adult Events",
          eventdesc: "Celebrate your special event with a Fun!",
          eventimg: "events/sip.webp",
          url: "/adultevent",
          link: "Adult Events",
        },
        {
          id: 5,
          eventtitle: "Adult Classes",
          eventdesc: "Enjoy special classes  with us!",
          eventimg: "events/yoga.webp",
          url: "/adultclass",
          link: "Adult Classes",
        },
      ],
    };
  },
  mounted() {},
};
</script>
