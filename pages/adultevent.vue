<template>
  <div>
    <Navlink />

    <div class="events row-grid">
      <div class="separt2 row-grid">
        <div class="container">
          <h1>Adults Events</h1>
          <!-- <img
            class="wed-img1 row-grid row-bottom-grid"
            src="../assets/img/events/Corporate Cocktail Event (2).jpg"
            alt=""
          /> -->
          <div class="box"></div>
        </div>
      </div>
      <div class="container">
        <div class="wedding-event">
          <div class="wrapper">
            <div class="wed-offer">
              <h2>Sip N Paint</h2>
            </div>
            <div class="small-offer">
              <div class="single-offer">
                <img src="../assets/img/events/sip.webp" alt="" />
              </div>
              <div class="single-offer">
                <img src="../assets/img/events/sip2.jpg" alt="" />
              </div>
              <div class="single-offer">
                <img src="../assets/img/events/sip3.jpg" alt="" />
              </div>
              <div class="single-offer">
                <img src="../assets/img/events/sip4.jpg" alt="" />
              </div>
            </div>
            <div class="wed-offer">
              <h2>Coprate Events</h2>
            </div>
            <div class="small-offer">
              <div class="single-offer">
                <img src="../assets/img/events/coporate.webp" alt="" />

                <p></p>
              </div>
              <div class="single-offer">
                <img src="../assets/img/events/CorporateEvent.jpg" alt="" />

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

    <!-- <div class="events2 row-grid">
        <div class="separt2 row-grid">
          <div class="container"></div>
        </div>
        <div class="container">
          <h4>Book Now</h4>
        </div>
      </div> -->
    <div class="cta-register row-max-grid">
      <div class="container2">
        <h1>Book Now</h1>
        <div class="separt-line"></div>
        <Videocop video="746055968" />
        <!-- <img src="../assets/img/events/coporate.webp" alt="" /> -->
       
        <p>
          If you are interested in our adults events and wants to book, contact us to secure your spot with us!
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
          eventtitle: "Birthday",
          eventdesc:
            "Celebrate your special day with a Birthday Dance Party! 3 Hours of Dancing & Fun!",
          eventimg: "program/gal6.webp",
          offer1: "Party clean-up",
          offer2: "3 hours of party time",
          offer3:
            "1 hour of enthusiastic, positive and high-quality dance instruction",
          offer4:
            "A final show at the end of the party to entertain parents with all we've learned",
          offer5: "Special gift for the birthday star",
          offer6: "Party Table, cake table and table covering",
        },
        {
          id: 2,
          eventtitle: "Graduation",
          eventdesc: "Celebrate your special day with Fun!",
          eventimg: "events/ICS.webp",
        },
        {
          id: 3,
          eventtitle: "Corporate Events ",
          eventdesc: "Corporate Events (KEFITA)",
          eventimg: "events/coporate.webp",
        },
        {
          id: 6,
          eventtitle: "Wedding",
          eventdesc: "Celebrate your special event with a Dancing & Fun!",
          eventimg: "events/wed.webp",
        },
        {
          id: 4,
          eventtitle: "Sip and Paint",
          eventimg: "events/sip.webp",
        },
        {
          id: 5,
          eventtitle: "Yoga",

          eventimg: "events/yoga.webp",
        },
      ],
    };
  },
  mounted() {},
};
</script>
