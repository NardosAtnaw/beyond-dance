<template>
  <div>
    <Navlink />

    <Homevideo video="744959148" class="row-grid" />
    <div class="join-cta row-max-grid">
      <div class="container">
        <div class="bg-texture">
          <img src="../assets/img/texture.svg" alt="" />
        </div>
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
          <button class="btn btn-primary row-grid">Register Now</button>
        </div>
      </div>
    </div>

    <div class="who-we-are row-max-grid">
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
            <!-- <button class="btn btn-secondary">Discover More</button> -->
          </div>
        </div>
      </div>
    </div>

    <div class="big-image row-grid">
      <img src="../assets/img/showcase2.JPG" alt="" />
    </div>
    <div class="programs row-max-grid">
      <div class="container">
        <h1>Programs</h1>
        <div class="schedule-all row-max-grid">
          <div class="sch-title">
            <h2>Schedule</h2>
            <div class="decor-box"></div>
          </div>
          <Schedule />
        </div>
        <div class="class-all row-max-grid">
          <div class="class-title">
            <h2>Classes</h2>
            <div class="decor-box"></div>
            <div class="class-list">
              <div class="class-single row-max-grid">
                <img src="../assets/img/takwalogo.svg" alt="" />
                <h3 class="row-grid">TAEKWONDO</h3>
                <p class="row-grid">
                  Taekwondo is a system of symmetrical body exercises or
                  techniques designed for self-defense and counter attack in
                  unarmed combat
                </p>
              </div>
              <div class="class-single row-max-grid">
                <img src="../assets/img/hiphoplogo.svg" alt="" />
                <h3 class="row-grid">HIP HOP</h3>
                <p class="row-grid">
                  Hip Hop is very unique, as it allows its dancers to perform
                  with freedom of movement, adding in their own personalities.
                </p>
              </div>
              <div class="class-single row-max-grid">
                <img src="../assets/img/gymlogo.svg" alt="" />
                <h3 class="row-grid">GYMNASTICS</h3>
                <p class="row-grid">
                  Gymnastics is a sport that includes physical exercises
                  requiring balance, strength, flexibility, agility,
                  coordination, dedication and endurance.
                </p>
              </div>
              <div class="class-single row-max-grid">
                <img src="../assets/img/yogalogo.svg" alt="" />
                <h3 class="row-grid">YOGA</h3>
                <p class="row-grid">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Necessitatibus, veniam! Commodi atque laboriosam officia.
                  Doloribus animi perspiciatis nam, quod hic debitis .
                </p>
              </div>
              <div class="class-single row-max-grid">
                <img src="../assets/img/balletlogo.svg" alt="" />
                <h3 class="row-grid">BALLET</h3>
                <p class="row-grid">
                  The focus will be set on placement, alignment, flexibility and
                  musicality through a blend of traditional ballet techniques.
                  As students’ progress through the levels
                </p>
              </div>
              <div class="class-single row-max-grid">
                <img src="../assets/img/painologo.svg" alt="" />
                <h3 class="row-grid">PAINO</h3>
                <p class="row-grid">
                  Students learn basic piano skills and fundamentals of music
                  literacy, including basic notation, rhythms, time signatures,
                  and intervals.
                </p>
              </div>
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
};
</script>
