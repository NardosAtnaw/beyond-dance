<template>
  <div>
    <Navlink />

    <div class="classes row-max-grid">
      <div class="container">
        <!-- <h1>Classes</h1> -->
        <div class="class-wrapper" v-for="item in classes" :key="item.id">
          <div class="single-class row-grid">
            <div class="class-title">
              <h2>{{ item.title }}</h2>
              <p>
                {{ item.desc }}
              </p>

              <button class="btn row-grid btn-purple">Register Now</button>
            </div>
            <div class="separt-line"></div>
            <div class="class-desc">
              <div class="class-img row-grid">
                <img :src="require('@/assets/img/' + item.img1 + '')" alt="" />
                <img :src="require('@/assets/img/' + item.img2 + '')" alt="" />
                <img :src="require('@/assets/img/' + item.img3 + '')" alt="" />
                <img :src="require('@/assets/img/' + item.img4 + '')" alt="" />
              </div>
            </div>
          </div>
          <div class="single-class1 row-grid">
            <div class="class-desc">
              <div class="class-img row-grid">
                <img :src="require('@/assets/img/' + item.img12 + '')" alt="" />
                <img :src="require('@/assets/img/' + item.img22 + '')" alt="" />
                <img :src="require('@/assets/img/' + item.img32 + '')" alt="" />
                <img :src="require('@/assets/img/' + item.img42 + '')" alt="" />
              </div>
            </div>
            <div class="separt-line"></div>
            <div class="class-title">
              <h2>{{ item.title2 }}</h2>
              <p>
                {{ item.desc2 }}
              </p>

              <button class="btn row-grid btn-purple">Register Now</button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="schedule-all1 row-max-grid">
      <div class="container">
        <div class="sch-title">
          <h1>Schedule</h1>
          <!-- <div class="decor-box1"></div> -->
        </div>
        <Schedule />
      </div>
    </div>

    <div class="pro-gallery row-max-grid row-bottom-grid">
      <div class="container">
        <h1>Gallery</h1>
        <div class="gallery-wrapper row-grid">
          <div
            class="single-img row-grid"
            v-for="item in gallery"
            :key="item.id"
          >
            <img :src="require('@/assets/img/' + item.img + '')" alt="" />
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Schedule from "../components/Schedule.vue";
export default {
  data() {
    return {
      classes: [
        {
          title: "Ballet",
          desc: " The focus will be set on placement, alignment, flexibility and musicality through a blend of traditional ballet techniques. As students’ progress through the levels, the exercises will increase in length and difficulty and more emphasis will be placed on retention of choreography and performance quality.",
          img1: "ballet.JPG",
          img2: "ballet1.JPG",
          img3: "ballet2.JPG",
          img4: "ballet5.JPG",
          title2: "Jazz",
          desc2:
            " Standard jazz combinations will be taught to a mixture of traditional jazz, Broadway and popular music. Vocabulary that is specific to jazz dance includes syncopated rhythm, isolations, turns, large jumps, leaps and many technical elements.",
          img12: "jazz5.JPG",
          img22: "jazz3.JPG",
          img32: "jazz4.JPG",
          img42: "jazz2.JPG",
        },
        {
          title: "Hip Hop",
          desc: " The focus will be set on placement, alignment, flexibility and musicality through a blend of traditional ballet techniques. As students’ progress through the levels, the exercises will increase in length and difficulty and more emphasis will be placed on retention of choreography and performance quality.",
          img1: "hiphop.jpg",
          img2: "gal2.jpg",
          img3: "hiphop2.jpg",
          img4: "hiphop.jpg",
          title2: "Lyrical / CO",
          desc2:
            " The focus will be set on placement, alignment, flexibility and musicality through a blend of traditional ballet techniques. As students’ progress through the levels, the exercises will increase in length and difficulty and more emphasis will be placed on retention of choreography and performance quality.",
          img12: "showcase30.jpg",
          img22: "showcasse10.jpg",
          img32: "showcase2.JPG",
          img42: "showcase11.jpg",
        },
        {
          title: "Takewando",
          desc: " Taekwondo is a system of symmetrical body exercises or techniques designed for self-defense and counterattack in unarmed combat, making use of the hands and feet as weapons and defenses. However, Taekwondo is not merely a physical skill; it is also a way of thought and life. Through strict discipline, Taekwondo trains both the body and the mind placing great emphasis on the development of moral character. ",
          img1: "gal4.JPG",
          img2: "gal9.JPG",
          img3: "Take2.jpg",
          img4: "Take3.jpg",
          title2: "Summer Camp",
          desc2:
            "Our experienced and loving instructors have prepared an annual creative camp for all ages and levels this summer. Sign your dancer up today, bring a friend and make summer extra fun!!",
          img12: "Summer1.jpg",
          img22: "Summer2.jpg",
          img32: "Summer4.jpg",
          img42: "Summer3.JPG",
        },
        {
          title: "Gymnastics",
          desc: "Gymnastics is a sport that includes physical exercises requiring balance, strength, flexibility, agility, coordination, dedication and endurance. The movements involved in gymnastics contribute to the development of the arms, legs, shoulders, back, chest, and abdominal muscle groups ",
          img1: "Studio1.jpg",
          img2: "gal9.JPG",
          img3: "gym2.webp",
          img4: "Studio2.jpg",
          title2: "Drawing",
          desc2:
            "A form of visual art in which our students use instruments to mark paper or other two-dimensional surface. It is generally concerned with the marking of lines and areas of tone onto paper/other material, where the accurate representation of the visual world is expressed upon a plane surface.",
          img12: "Drawing1.JPG",
          img22: "Drawing2.jpg",
          img32: "Drawing3.jpg",
          img42: "Drawing4.jpg",
        },
        {
          title: "Traditional Dance",
          desc: " Each of the Ethiopian traditional dances has unique body movements and steps. Our students will be able to explore different cultural dances.",
          img1: "traditional.webp",
          img2: "traditional2.jpg",
          img3: "traditional3.jpg",
          img4: "traditional4.jpg",
          title2: "Piano",
          desc2:
            "students learn basic piano skills and fundamentals of music literacy, including basic notation, rhythms, time signatures, and intervals.",
          img12: "paino.jpg",
          img22: "paino2.jpeg",
          img32: "Studio1.jpg",
          img42: "paino3.jpg",
        },
      ],

      gallery: [
        {
          id: 1,
          img: "gal1.jpg",
        },
        {
          id: 2,
          img: "gal2.jpg",
        },
        {
          id: 3,
          img: "gal3.jpg",
        },
        {
          id: 4,
          img: "gal4.JPG",
        },
        {
          id: 5,
          img: "gal5.JPG",
        },
        {
          id: 6,
          img: "gal6.jpg",
        },
        {
          id: 7,
          img: "gal7.jpg",
        },
        {
          id: 8,
          img: "gal8.JPG",
        },
        {
          id: 9,
          img: "gal9.JPG",
        },
        // {
        //   id: 10,
        //   img: "gal10.jpg",
        // },
        // {
        //   id: 11,
        //   img: "gal11.JPG",
        // },
        // {
        //   id: 12,
        //   img: "gal12.jpg",
        // },
      ],
    };
  },
  mounted() {},
  components: { Schedule },
};
</script>
