<template>
  <div>
    <Navlink />
    <!-- <Homevideo video="744993912" class="row-grid" /> -->
    <div class="about-all row-grid">
      <div class="container">
        <div class="about-wrapper">
          <Aboutvideo video="744979888" class="video" />

          <div class="about-txt">
            <h2>About Us</h2>
            <p>
              Beyond Dance Studio is the first of its kind in Ethiopia offering
              a wide range of kids dance, martial arts and instrumental classes
              from Ballet, Jazz, Taekwondo, Piano and Beyond. Our vision is to
              introduce the joy of dance to hundreds of children across Addis
              Ababa. We grow our students to become confident, creative and
              courageous individuals who make lasting memories along the
              way. Beyond Dance's vision is to introduce the joy of dance to
              hundreds of children across Addis Ababa. When you decide to join
              us at Beyond Dance, you too will be able to take advantage of our
              professional staff at our fully-equipped and recently renovated
              studio. Whether you're a beginner or an experienced dancer looking
              to improve your technique, we guarantee you'll find it here. 
            </p>
            <button class="btn btn-thrid">
              <a href="contactus">Contact Us</a>
            </button>
          </div>
        </div>
      </div>
    </div>

    <div class="faq row-max-grid">
      <div class="container">
        <h1>Frequently Asked Questions</h1>
        <div class="faq-wrapper">
          <div class="faq-accordo row-grid">
            <div id="wrapper" :data="accordion">
              <ul>
                <li v-for="items in accordion" :key="items.id">
                  <input type="checkbox" checked />
                  <i></i>
                  <h2>
                    <span class="ques-p">{{ items.question }}</span>
                  </h2>
                  <p>{{ items.answer }}</p>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="separt row-max-grid">
      <div class="container">
        <div class="box"></div>
      </div>
    </div>
    <div class="safty row-max-grid">
      <div class="container">
        <h2>Beyond Dance Studio Rules</h2>
        <div class="list-safty">
          <div class="studio-safty row-grid">
            <ul :data="studiosafty">
              <li v-for="item in studiosafty" :key="item.id">
                <a href=""
                  ><p class="row-grid">{{ item.rule }}</p></a
                >
              </li>
            </ul>
          </div>
          <!-- <div class="covid-safty row-grid">
            <h3>Studio Safety for Covid-19</h3>
            <ul :data="covidsafty">
              <li v-for="item in covidsafty" :key="item.id">
                <a href=""
                  ><p class="row-grid">{{ item.rule }}</p></a
                >
              </li>
            </ul>
          </div> -->
        </div>
        <div class="download-mid row-max-grid">
          <p class="">
            Click the link below to get a PDF of our safety and regulation to
            learn about the security of our studio.
          </p>
          <button class="btn btn-secondary row-grid">
            <a href="../../Safety.pdf" target="_blank" download> Download Safety</a>
          </button>
        </div>
      </div>
    </div>

    <section class="dance-wear row-max-grid">
      <div class="container">
        <h2>Dancewear and Apparel</h2>
        <p class="frist-p">
          See the Dancewear and Apparel below to get your and contact us.
        </p>
        <div class="dance-wear-wrapper">
          <div class="dance-wear-items">
            <div
              class="single-item row-grid"
              v-for="item in dancewear"
              :key="item.id"
            >
              <img
                class="bigimg"
                :src="require('@/assets/img/' + item.bigimage + '')"
                alt=""
              />

              <div class="right-table">
                <h4>{{ item.itemname }}</h4>
                <!-- <p>{{ item.itemdesc }}</p> -->
                <div class="images">
                  <img
                    :src="require('@/assets/img/' + item.img1 + '')"
                    alt=""
                  />
                  <img
                    :src="require('@/assets/img/' + item.img2 + '')"
                    alt=""
                    v-if="item.img2"
                  />
                  <img
                    :src="require('@/assets/img/' + item.img3 + '')"
                    alt=""
                    v-if="item.img3"
                  />
                </div>
                <button class="btn btn-primary">
                  <nuxt-link to="/contactus">Contact Us to Order </nuxt-link>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <div class="gallery row-bottom-grid">
      <div class="container">
        <h1>Dance Studios</h1>
        <div class="gallery-wrapper row-grid">
          <div
            class="single-img row-grid"
            v-for="item in gallery"
            :key="item.id"
          >
            <img :src="require('@/assets/img/' + item.img + '')" alt="" />
            <p class="studio-name">{{ item.studioname }}</p>
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
      accordion: [
        {
          id: 1,
          question: " Can I sign my child up for multiple classes?",
          answer:
            "Of course! We recommend signing up for multiple styles to find out what style your child prefers.",
        },
        {
          id: 2,
          question: "Are uniforms mandatory?",
          answer:
            "Yes. We require uniforms in all class styles except for Hip Hop. If you don't own the proper uniform you can purchase it at Beyond Dance Studio.",
        },
        {
          id: 3,
          question: " Can I register for only one month of classes?",
          answer:
            "Unfortunately we do not offer this. Our season is a full 4 month commitment, our reason being that we want full dedication and commitment. ",
        },
        {
          id: 4,
          question:
            "If I am out of the country and comeback after class starts can I still sign up for class?",
          answer:
            "Yes! We cannot promise the class you want will be available, so we recommend you securing your spot in any means possible as soon as possible!",
        },
      ],
      studiosafty: [
        {
          id: 1,
          rule: "Lobby is CLOSED except for Payments, Uniforms, Personal Matter ",
        },
        {
          id: 2,
          rule: "Maximum 5 Parents or Guardians allowed in Studio Lobby",
        },

        {
          id: 3,
          rule: "Drop Off should be at Beyond Dance Studio Main Door",
        },
        {
          id: 4,
          rule: "Pick Up should be at Beyond Dance Studio Main Door (Sign out)",
        },
        {
          id: 5,
          rule: "Parents will be asked to drop off their children on time",
        },
        {
          id: 6,
          rule: "Pick them up 5 minutes before class ends",
        },
        {
          id: 7,
          rule: "Masks are MANDATORY at all times in the studio ( Ages 6+ )",
        },
        {
          id: 8,
          rule: "Students should bring their own reusable water bottles",
        },
      ],

      dancewear: [
        {
          id: 8,
          itemname: "Leotard",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "dancestudio/DanceWear.webp",
          img1: "dancestudio/Leotard.webp",
          img2: "dancestudio/DanceWear.webp",
        },
        {
          id: 1,
          itemname: "Athletic Leggings",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "dancestudio/leggingbig.webp",
          img1: "dancestudio/legg1.webp",
          img2: "dancestudio/legg2.webp",
        },

        {
          id: 2,
          itemname: "Waist Trainer",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "dancestudio/waistbig.webp",
          img1: "dancestudio/waist1.webp",
          img2: "dancestudio/waist2.webp",
          img3: "dancestudio/waist3.webp",
        },
        {
          id: 3,
          itemname: "Athletic Wear",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "dancestudio/athwearbig.webp",
          img1: "dancestudio/ath1.webp",
          img2: "dancestudio/ath2.webp",
          img3: "dancestudio/ath3.webp",
        },
        {
          id: 4,
          itemname: "Athletic Top Wear",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "dancestudio/athtopwear.webp",
          img1: "dancestudio/topwear1.webp",
          img2: "dancestudio/top2.webp",
          img3: "dancestudio/top3.webp",
        },
        {
          id: 5,
          itemname: "Athletic Top Wear",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "dancestudio/bigtop.webp",
          img1: "dancestudio/1top.webp",
        },
        {
          id: 6,
          itemname: "Athletic Zip Up Jacket",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "dancestudio/zipjacketbig.webp",
          img1: "dancestudio/zipjacket1.webp",
        },
      ],
      gallery: [
        {
          id: 1,
          img: "dancestudio/Studio1.webp",
          studioname: "Studio 1",
        },
        {
          id: 2,
          img: "dancestudio/Studio2.webp",
          studioname: "Studio 2",
        },
        {
          id: 3,
          img: "dancestudio/Studio3.webp",
          studioname: "Studio 3",
        },
      ],
    };
  },
  mounted() {},
};
</script>
