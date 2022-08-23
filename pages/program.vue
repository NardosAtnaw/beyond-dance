<template>
  <div>
    <Navlink />
    <div class="about-us row-max-grid">
      <div class="container">
        <h1 class="row-max-grid">About Us</h1>

        <div class="desc-about">
          <div class="about-txt row-max-grid">
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
            <button class="btn btn-primary">Contact Us</button>
          </div>
          <div class="about-image">
            <img src="../assets/img/Takewoado.jpg" alt="" />
          </div>
        </div>
      </div>
    </div>
    <div class="faq row-max-grid">
      <div class="container">
        <div class="faq-texture">
          <img src="../assets/img/faqbg.svg" alt="" />
        </div>
        <h1>Frequently Asked Questions</h1>
        <div class="faq-wrapper">
          <div class="faq-accordo">
            <div id="wrapper" :data="accordion">
              <ul>
                <li v-for="items in accordion" :key="items.id">
                  <input type="checkbox" checked />
                  <i></i>
                  <h2>
                   <span class="ques-p">{{ items.question }}</span> 
                    <span class="plus-icon">+</span>
                  </h2>
                  <p>{{ items.answer }}</p>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
        <section class="dance-wear row-bottom-grid row-max-grid">
      <div class="container">
        <h2 >Dancewear and Apparel</h2>
        <p class="frist-p row-grid">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean
          accumsan pretium tortor, in Lorem ipsum dolor sit amet, consectetur
        </p>
        <div class="dance-wear-wrapper">
          <div class="dance-wear-items">
            <div
              class="single-item row-max-grid"
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
                <p>{{ item.itemdesc }}</p>
                <div class="images">
                  <img
                    :src="require('@/assets/img/' + item.img1 + '')"
                    alt=""
                  />
                  <img
                    :src="require('@/assets/img/' + item.img2 + '')"
                    alt=""
                  />
                  <img
                    :src="require('@/assets/img/' + item.img3 + '')"
                    alt=""
                  />
                </div>
                <button class="btn btn-primary">Order Now</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <div class="separt row-max-grid">
      <div class="container">
        <div class="box"></div>
      </div>
    </div>
    <div class="safty row-max-grid">
      <div class="container">
        <h2>Studio Safty</h2>
        <div class="list-safty">
          <div class="studio-safty row-grid">
            <h3>Dance Studio Safty Rule</h3>
            <ul :data="studiosafty">
              <li v-for="item in studiosafty" :key="item.id">
                <a href=""
                  ><p class="row-grid">{{ item.rule }}</p></a
                >
              </li>
            </ul>
          </div>
          <div class="covid-safty row-grid">
            <h3>Studio Safty for Covid-19</h3>
            <ul :data="covidsafty">
              <li v-for="item in covidsafty" :key="item.id">
                <a href=""
                  ><p class="row-grid">{{ item.rule }}</p></a
                >
              </li>
            </ul>
          </div>
        </div>
        <div class="download-mid row-max-grid">
          <p class="">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean
            accumsan pretium tortor, in Lorem ipsum dolor sit amet, consectetur
          </p>
          <button class="btn btn-secondary row-grid">Download PDF</button>
        </div>
      </div>
    </div>

    <div class="gallery row-max-grid row-bottom-grid">
      <div class="container">
        <h1>Gallery</h1>
        <div class="gallery-wrapper row-grid">
          <div class="single-img row-grid" v-for="item in gallery" :key="item.id">
           <img
                    :src="require('@/assets/img/' + item.img + '')"
                    alt=""
                  />
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  data() {
    return {
    
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
            {
          id: 10,
          img: "gal10.jpg",
        },
                {
          id: 11,
          img: "gal11.JPG",
        },
            {
          id: 12,
          img: "gal12.jpg",
        },
      ],
    };
  },
  mounted() {},
};
</script>
