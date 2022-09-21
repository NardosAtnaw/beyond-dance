<template>
  <div>
    <Navlink />

    <Homevideo video="744993912" class="row-grid" />
    <!-- <img class="bg-back" src="../assets/img/texture.svg" alt="" /> -->
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
          <button class="btn row-grid btn-purple">
            <nuxt-link to="/register">Register Now </nuxt-link>
          </button>
        </div>
        <div class="join-img">
          <img src="../assets/img/home/jointoday.webp" alt="" />
        </div>
      </div>
    </div>
    <div class="who-we-are row-max-grid">
      <div class="container">
        <div class="who-all">
          <div class="who-title"></div>
          <div class="who-desc">
            <img src="../assets/img/home/whoweare.webp" alt="" />
            <div class="desc-p">
              <h1>Who We Are</h1>

              <p>
                Beyond Dance Studio is the first of its kind in Ethiopia
                offering a wide range of kids dance, martial arts and
                instrumental classes from Ballet, Jazz, Taekwondo, Piano and
                Beyond. Our vision is to introduce the joy of dance to hundreds
                of children across Addis Ababa. We grow our students to become
                confident, creative and courageous individuals who make lasting
                memories along the way. Beyond Dance’s vision is to introduce
                the joy of dance to hundreds of children across Addis Ababa.
                When you decide to join us at Beyond Dance, you too will be able
                to take advantage of our professional staff at our
                fully-equipped and recently renovated studio. Whether you’re a
                beginner or an experienced dancer looking to improve your
                technique, we guarantee you’ll find it here.
              </p>
              <button class="btn btn-thrid">
                <a href="dancestudio">Discover More</a>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="class-all row-max-grid">
      <div class="container">
        <div class="class-title">
          <h2>Classes</h2>
          <!-- <div class="separt1">
            <div class="container">
              <div class="box"></div>
            </div>
          </div> -->

          <div>
            <a class="grid" href="/program">
              <figure
                class="effect-bubba"
                v-for="item in homeclass"
                :key="item.id"
              >
                <img
                  class="img-logo"
                  :src="require('@/assets/img/' + item.img + '')"
                  alt=""
                />

                <figcaption>
                  <h2>{{ item.title }}</h2>
                  <p>
                    {{ item.desc }}
                  </p>
                </figcaption>
              </figure></a
            >
          </div>

          <div class="class-note row-max-grid">
            <p>
              Click the button below to register for classes and view
              descriptions of all programs, including ballet, taekwondo, jazz,
              and other classes..
            </p>
            <button class="btn btn-thrid row-grid">
              <nuxt-link to="/program">See all the program </nuxt-link>
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="schedule-show row-max-grid">
      <div class="container">
        <h2>Schedule</h2>
        <!-- <div class="decor-box"></div> -->
        <div class="separt1">
          <div class="container">
            <div class="box"></div>
          </div>
        </div>
        <img class="row-grid" src="../assets/img/home/sum.webp" alt="" />
        <div class="sche-note row-grid">
          <p>
            Please click the button below to download the schedule, which is
            displayed in full in an image.
          </p>
          <div>
            <button class="btn btn-thrid row-grid">
              <nuxt-link to="/program">See all the program </nuxt-link>
            </button>
            <button class="btn btn-secondary row-grid">
              <a href="Schedule.png" target="_blank" download>
                Download Schedule</a
              >
            </button>
          </div>
        </div>
      </div>
    </div>

    <div class="show-case row-max-grid row-bottom-grid">
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

    <section class="map">
      <div class="container">
        <h1 class="title center">Get Our Location</h1>
        <p class="text center">
          If you want to register or contact us in person here is the link for
          our location.
        </p>
        <div class="separt1">
          <div class="container">
            <div class="box"></div>
          </div>
        </div>

        <div class="map-container">
          <div class="location">
            <div class="map-responsive">
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3940.7979184031483!2d38.78157451478621!3d8.9907343935474!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x164b85365f26ad5b%3A0x9f836f1aa87df253!2sBeyond%20Dance%20Studio!5e0!3m2!1sen!2set!4v1662642722811!5m2!1sen!2set"
                width="600"
                height="450"
                style="border: 0"
                allowfullscreen=""
                loading="lazy"
                referrerpolicy="no-referrer-when-downgrade"
              ></iframe>
            </div>
          </div>
        </div>
      </div>
    </section>
    <Contactus />
    <div class="try-hover"></div>

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
          img: "balletlogo.svg",
          title: "Ballet",
          desc: "The focus will be set on placement, alignment, flexibility and musicality through a blend of traditional ",
        },
        {
          img: "takwalogo.svg",
          title: "Taekwondo",
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
          img: "painologo.svg",
          title: "Piano",
          desc: " Students learn basic piano skills and fundamentals of music literacy, including basic notation, rhythms, ....",
        },
      ],
    };
  },
};
</script>
