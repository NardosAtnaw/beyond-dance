<template>
  <div>
    <Navlink />
      <div class="big-image row-grid">
        <div class="container">
      <img src="../assets/img/showcase2.JPG" alt="" />
        </div>


    </div>
    <div class="events row-max-grid ">
      <div class="container">
        <div class="event-wrapper">
          <div
            class="single-event row-grid"
            v-for="item in events"
            :key="item.id"
          >
            <img :src="require('@/assets/img/' + item.eventimg + '')" alt="" />
            <div class="all-txt">

            <h2 >{{ item.eventtitle }}</h2>
            <p >{{ item.eventdesc }}</p>

            <ul>
              <h4 >What We Offer</h4>
              <li >{{ item.offer1 }}</li>
              <li >{{ item.offer2 }}</li>
              <li>{{ item.offer3 }}</li>
              <li>{{ item.offer4 }}</li>
              <li>{{ item.offer5 }}</li>
              <li>{{ item.offer6 }}</li>
            </ul>
        
            </div>

          </div>
        </div>
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
          eventimg: "gal6.jpg",
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
          eventdesc: "Celebrate your special day with a Dancing & Fun!",
          eventimg: "ICS.jpg",
          offer1: "Lorem ipsum dolor sit amet",
          offer2: "Lorem ipsum dolor sit amet",
          offer3: "Lorem ipsum dolor sit amet",
          offer4: "Lorem ipsum dolor sit amet",
          offer5: "Lorem ipsum dolor sit amet",
          offer6: "Lorem ipsum dolor sit amet",
        },
        {
          id: 3,
          eventtitle: "Corporate Events ",
          eventdesc: "Corporate Events (KEFITA)",
          eventimg: "KEFITA.webp",
          offer1: "Lorem ipsum dolor sit amet",
          offer2: "Lorem ipsum dolor sit amet",
          offer3: "Lorem ipsum dolor sit amet",
          offer4: "Lorem ipsum dolor sit amet",
          offer5: "Lorem ipsum dolor sit amet",
          offer6: "Lorem ipsum dolor sit amet",
        },
        {
          id: 4,
          eventtitle: "Sip and Paint",
          eventdesc: "Celebrate your special event with a Dancing & Fun!",
          eventimg: "sipnpaint.jpg",
          offer1: "Lorem ipsum dolor sit amet ",
          offer2: "Lorem ipsum dolor sit amet",
          offer3: "Lorem ipsum dolor sit amet",
          offer4: "Lorem ipsum dolor sit amet",
          offer5: "Lorem ipsum dolor sit amet",
          offer6: "Lorem ipsum dolor sit amet",
        },
      ],
    };
  },
  mounted() {},
};
</script>
