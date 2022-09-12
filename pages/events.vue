<template>
  <div>
    <Navlink />

    <Homevideo video="744993912" class="row-grid" />

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
            <div class="wed-offer">
              <h2>Wedding Package Details</h2>
            </div>
            <div class="small-offer">
              <div class="single-offer">
                <img src="../assets/img/events/slowdance.webp" alt="" />
                <h4>Slow Dance</h4>
                <p>Couples choreographed & Group practice</p>
              </div>
              <div class="single-offer">
                <img src="../assets/img/events/wedtraditional.webp" alt="" />
                <h4>Traditional Dance</h4>
                <p>Couples Practice & Group Practice</p>
              </div>
              <div class="single-offer">
                <img src="../assets/img/events/briddance.webp" alt="" />
                <h4>Bridal Group Performance</h4>
                <p>Group & 4 sessions (1 hour each)</p>
              </div>
              <div class="single-offer">
                <img src="../assets/img/events/groomdance.webp" alt="" />
                <h4>Groomsman Group Performance</h4>
                <p>Group & 3 sessions (1 hour each)</p>
              </div>
              <div class="single-offer">
                <img src="../assets/img/events/bgworkout.webp" alt="" />
                <h4>Bride/Groom 1 month/3 month Fitness Program</h4>
                <p>
                  Waist trainer (Bride)<br />
                  Group Fitness Classes<br />
                  Personal Training<br />
                  Diet Plan<br />
                  Weekly Check In<br />
                </p>
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
    <div class="events2 row-grid">
      <div class="separt2 row-grid">
        <div class="container"></div>
      </div>
      <div class="container">
        <div class="event-wrapper">
          <div
            class="single-event row-grid"
            v-for="item in events"
            :key="item.id"
          >
            <img :src="require('@/assets/img/' + item.eventimg + '')" alt="" />
            <div class="all-txt">
              <h2>{{ item.eventtitle }}</h2>
              <p>{{ item.eventdesc }}</p>

              <ul>
                <li>{{ item.offer1 }}</li>
                <li>{{ item.offer2 }}</li>
                <li>{{ item.offer3 }}</li>
                <li>{{ item.offer4 }}</li>
                <li>{{ item.offer5 }}</li>
                <li>{{ item.offer6 }}</li>
              </ul>
            </div>
          </div>
        </div>
        <div class="bottom-info">
          <p class="book-btn row-max-grid">
            Please get in touch with us via the form or in person if you want to
            get the service or participate in the activities.
          </p>
          <button class="btn btn-secondary">
            <a href="contactus"> Contact us to Book </a>
          </button>
        </div>
      </div>
    </div>
    <!-- <div class="separt1 row-grid">
      <div class="container">
        <div class="box"></div>
      </div>
    </div> -->
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
