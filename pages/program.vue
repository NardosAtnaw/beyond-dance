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

              <button class="btn row-grid btn-purple">
                <nuxt-link to="/register">Register Now </nuxt-link>
              </button>
            </div>
            <div class="separt-line"></div>
            <div class="class-desc">
              <div class="class-img row-grid">
                <img :src="require('@/assets/img/' + item.img1 + '')" alt="" />
                <img :src="require('@/assets/img/' + item.img2 + '')" alt="" />
          
              </div>
            </div>
          </div>
          <div class="single-class1 row-grid">
            <div class="class-desc">
              <div class="class-img row-grid">
                <img :src="require('@/assets/img/' + item.img12 + '')" alt="" />
                <img :src="require('@/assets/img/' + item.img22 + '')" alt="" />
           
              </div>
            </div>
            <div class="separt-line"></div>
            <div class="class-title">
              <h2>{{ item.title2 }}</h2>
              <p>
                {{ item.desc2 }}
              </p>

              <button class="btn row-grid btn-purple">
                <nuxt-link to="/register">Register Now </nuxt-link>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="programs row-max-grid">
      <div class="container">
        <div class="schedule-all row-max-grid">
          <div class="sch-title">
            <h2>Schedule</h2>
          </div>
          <Schedule />
        </div>
      </div>
    </div>

    <div class="pro-gallery row-bottom-grid">
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
import Contactus from "./contactus.vue";
export default {
  data() {
    return {
      classes: [
        {
          title: "Ballet",
          desc: " The focus will be set on placement, alignment, flexibility and musicality through a blend of traditional ballet techniques. As students’ progress through the levels, the exercises will increase in length and difficulty and more emphasis will be placed on retention of choreography and performance quality.",
          img1: "program/ballet.webp",
          img2: "program/ballet2.webp",
 
          title2: "Taekwondo",
          desc2:
            " Taekwondo is a system of symmetrical body exercises or techniques designed for self-defense and counterattack in unarmed combat, making use of the hands and feet as weapons and defenses. However, Taekwondo is not merely a physical skill; it is also a way of thought and life. Through strict discipline, Taekwondo trains both the body and the mind placing great emphasis on the development of moral character. ",
          img12: "program/gal4.webp",
          img22: "program/Take3.webp",
        },
        {
          title: "Jazz",
          desc: " Standard jazz combinations will be taught to a mixture of traditional jazz, Broadway and popular music. Vocabulary that is specific to jazz dance includes syncopated rhythm, isolations, turns, large jumps, leaps and many technical elements.",
       
          img1: "program/jazz3.webp",
      
          img2: "program/jazz2.webp",
          title2: "Hip Hop",
          desc2:
            " The focus will be set on placement, alignment, flexibility and musicality through a blend of traditional ballet techniques. As students’ progress through the levels, the exercises will increase in length and difficulty and more emphasis will be placed on retention of choreography and performance quality.",
          img12: "program/hiphop.webp",
          img22: "program/gal2.webp",
     
        
        },
        {
          title: "Lyrical / CO",
          desc: " The focus will be set on placement, alignment, flexibility and musicality through a blend of traditional ballet techniques. As students’ progress through the levels, the exercises will increase in length and difficulty and more emphasis will be placed on retention of choreography and performance quality.",
          img1: "program/showcase30.webp",
          img2: "program/Contemporary.JPG",
        
          title2: "Summer Camp",
          desc2:
            "Our experienced and loving instructors have prepared an annual creative camp for all ages and levels this summer. Sign your dancer up today, bring a friend and make summer extra fun!!",
          img12: "program/Summer1.webp",
        
          img22: "program/Summer3.webp",
        },
        {
          title: "Gymnastics",
          desc: "Gymnastics is a sport that includes physical exercises requiring balance, strength, flexibility, agility, coordination, dedication and endurance. The movements involved in gymnastics contribute to the development of the arms, legs, shoulders, back, chest, and abdominal muscle groups ",
          img1: "program/gym1.webp",
          img2: "program/gym3.webp",
  
          title2: "Drawing",
          desc2:
            "A form of visual art in which our students use instruments to mark paper or other two-dimensional surface. It is generally concerned with the marking of lines and areas of tone onto paper/other material, where the accurate representation of the visual world is expressed upon a plane surface.",
       
          img12: "program/Drawing2.webp",
      
          img22: "program/Drawing4.webp",
        },
        {
          title: "Traditional Dance",
          desc: " Each of the Ethiopian traditional dances has unique body movements and steps. Our students will be able to explore different cultural dances.",
          img1: "program/traditional.webp",
        
          img2: "program/traditional2.webp",
          title2: "Piano",
          desc2:
            "students learn basic piano skills and fundamentals of music literacy, including basic notation, rhythms, time signatures, and intervals.",
          img12: "program/paino.webp",
 
          img22: "program/paino3.webp",
        },
      ],

      gallery: [
        {
          id: 1,
          img: "program/gal1.webp",
        },
        {
          id: 2,
          img: "program/gal2.webp",
        },
        {
          id: 3,
          img: "program/gal3.webp",
        },
        {
          id: 4,
          img: "program/gal4.webp",
        },
        {
          id: 5,
          img: "program/gal5.webp",
        },
        {
          id: 6,
          img: "program/gal6.webp",
        },
        {
          id: 7,
          img: "program/gal7.webp",
        },
        {
          id: 8,
          img: "program/gal8.webp",
        },
        {
          id: 9,
          img: "program/gal9.webp",
        },
        {
          id: 10,
          img: "program/gal10.webp",
        },
        {
          id: 11,
          img: "program/gal11.webp",
        },
        {
          id: 12,
          img: "program/gal12.webp",
        },
      ],
    };
  },
  mounted() {},
  components: { Schedule, Contactus },
};
</script>
