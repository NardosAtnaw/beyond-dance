<template>
  <div>
    <Navlink />

    <Homevideo video="744993912" class="row-grid" />
    <div class="who-we-are row-grid">
      <div class="container">
        <div class="who-all">
          <div class="who-title">
            <h1>Who We Are</h1>
          </div>
          <div class="who-desc">
            <p>
              Beyond Dance Studio is the first of its kind in Ethiopia offering
              a wide range of kids to young adult dance classes from ballet,
              jazz, hip hop, technique and beyond. We as a company are committed
              to grow your dancers at an accelerated rate through dedication and
              discipline. Beyond Dance’s vision is to introduce the joy of dance
              to hundreds of children across Addis Ababa. When you decide to
              join us at Beyond Dance, you too will be able to take advantage of
              our professional staff at our fully-equipped and recently
              renovated studio. Whether you’re a beginner or an experienced
              dancer looking to improve your technique, we guarantee you’ll find
              it here.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="join-cta row-max-grid">
      <div class="container">
        <div class="join-txt">
          <div class="join-title">
            <h1>Join Us Today!</h1>
          </div>
          <div class="join-p">
            <p>
              If you are interested in joining Beyond Dance Studio, we encourage
              you to pre-register to secure your spot with us!
            </p>
          </div>
          <button class="btn btn-thrid row-grid">Register Now</button>
        </div>
        <div class="join-img">
          <img src="../assets/img/showcase2.jpg" alt="" />
        </div>
      </div>
    </div>
    <div class="programs row-max-grid">
      <div class="container">
        <!-- <h1>Programs</h1> -->
        <div class="schedule-all row-max-grid">
          <div class="sch-title">
            <h2>Schedule</h2>
            <!-- <div class="decor-box"></div> -->
          </div>
          <Schedule />
        </div>
        <div class="class-all row-max-grid">
          <div class="class-title">
            <h2>Classes</h2>
            <!-- <div class="decor-box"></div> -->
            <div class="class-list">
              <div
                class="class-single row-max-grid"
                v-for="item in homeclass"
                :key="item.id"
              >
                <img :src="require('@/assets/img/' + item.img + '')" alt="" />
                <div class="decor-box"></div>
                <h3 class="row-grid">{{ item.title }}</h3>
                <p>
                  {{ item.desc }}
                </p>
              </div>
            </div>
            <div class="class-note row-max-grid">
              <p>
                Click the button below to view all programs and classes as well as to register.
              </p>
              <button class="btn btn-secondary row-grid">
                <a href="program"> See all the program</a>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="show-case row-max-grid">
      <div class="container">
        <h1>Show Case 2022</h1>

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
    <Contactus />
    <Footer />
  </div>
</template>

<script>
import Footer from "../components/Footer.vue";
import Schedule from "../components/Schedule.vue";
import Homevideo from "../components/Homevideo.vue";
export default {
  name: "IndexPage",
  components: { Footer, Schedule, Homevideo },

  data() {
    return {
      homeclass: [
        {
          img: "takwalogo.svg",
          title: "Takewondo",
          desc: "Taekwondo is a system of symmetrical body exercises or techniques designed for self-defense and counter...",
        },
        {
          img: "hiphoplogo.svg",
          title: "HIP HOP",
          desc: " Hip Hop is very unique, as it allows its dancers to perform with freedom of movement, adding in ...",
        },
        {
          img: "gymlogo.svg",
          title: "Gymnastics",
          desc: "Gymnastics is a sport that includes physical exercises requiring balance, strength, flexibility, agility,...",
        },
        {
          img: "yogalogo.svg",
          title: "Jazz",
          desc: "Standard jazz combinations will be taught to a mixture of traditional jazz, Broadway and popular music.",
        },
        {
          img: "balletlogo.svg",
          title: "Ballet",
          desc: "The focus will be set on placement, alignment, flexibility and musicality through a blend of traditional ",
        },
        {
          img: "painologo.svg",
          title: "Piano",
          desc: " Students learn basic piano skills and fundamentals of music literacy, including basic notation, rhythms, ....",
        },
      ],
    };
  },
};
</script>
