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
        <h1>Dance Studios</h1>
        <div class="gallery-wrapper row-grid">
          <div class="single-img row-grid" v-for="item in gallery" :key="item.id">
           <img
                    :src="require('@/assets/img/' + item.img + '')"
                    alt=""
                  />
                  <p class="studio-name">{{item.studioname}}</p>
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
      accordion: [
        {
          id: 1,
          question: " What is Lorem ipsum dolor sit ?",
          answer:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          id: 2,
          question: " Where is Lorem ipsum dolor sit ?",
          answer:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          id: 3,
          question: " How is Lorem ipsum dolor sit ?",
          answer:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          id: 4,
          question: " What is Lorem ipsum dolor sit ?",
          answer:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          id: 5,
          question: " How and where is Lorem ipsum ?",
          answer:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          id: 6,
          question: " How and where is Lorem ipsum ? ",
          answer:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          id: 7,
          question: "How and where is Lorem ipsum ?",
          answer:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
                {
          id: 8,
          question: " How and where is Lorem ipsum ?",
          answer:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          id: 9,
          question: " How and where is Lorem ipsum ? ",
          answer:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
        {
          id: 10,
          question: "How and where is Lorem ipsum ?",
          answer:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        },
      ],
      studiosafty: [
        {
          id: 1,
          rule: "Lorem ipsum dolor sit amet in culpa amet in culpa",
        },
        {
          id: 2,
          rule: "Lorem ipsum dolor sit amet in culpa amet in culpa",
        },
        {
          id: 3,
          rule: "Lorem ipsum dolor sit amet in culpa amet in culpa",
        },
        {
          id: 4,
          rule: "Lorem ipsum dolor sit amet in culpa amet in culpa",
        },
        {
          id: 5,
          rule: "Lorem ipsum dolor sit amet in culpa amet in culpa",
        },
        {
          id: 6,
          rule: "Lorem ipsum dolor sit amet in culpa amet in culpa",
        },
      ],
      covidsafty: [
        {
          id: 1,
          rule: "Lorem ipsum dolor sit consectetur ipsum dolor sit  ",
        },
        {
          id: 2,
          rule: "Lorem ipsum dolor sit ipsum dolor sit  consectetur ",
        },
        {
          id: 3,
          rule: "Lorem ipsum dolor sit  consectetur sit ipsum dolor ",
        },
        {
          id: 4,
          rule: "Lorem ipsum dolor sit ipsum dolor sit  consectetur ",
        },
        {
          id: 5,
          rule: "Lorem ipsum dolor sit  ipsum dolor sit  consectetur",
        },
        {
          id: 6,
          rule: "Lorem ipsum dolor sit consectetur ipsum dolor sit ",
        },
      ],
      dancewear: [
          {
          id: 1,
          itemname: "Athletic Leggings",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "leggingbig.jpg",
          img1: "legg1.jpg",
          img2: "legg2.jpg",
          img3: "legg1.jpg",
        },
    
        {
          id: 2,
          itemname: "Waist Trainer",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "waistbig.jpg",
          img1: "waist1.jpg",
          img2: "waist2.jpg",
          img3: "waist3.jpg",
        },
        {
          id: 3,
          itemname: "Athletic Wear",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "athwearbig.jpg",
          img1: "ath1.jpg",
          img2: "ath2.jpg",
          img3: "ath3.jpg",
        },
          {
          id: 4,
          itemname: "Athletic Top Wear",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "athtopwear.jpg",
          img1: "topwear1.jpg",
          img2: "top2.jpg",
          img3: "top3.jpg",
        },
        {
          id: 5,
          itemname: "Athletic Top Wear",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "bigtop.jpg",
          img1: "1top.jpg",
          img2: "2top.jpg",
          img3: "1top.jpg",
        },
        {
          id: 6,
          itemname: "Athletic Zip Up Jacket",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "zipjacketbig.jpg",
          img1: "zipjacket1.jpg",
          img2: "zipjacket1.jpg",
          img3: "zipjacket1.jpg",
        },
              {
          id: 7,
          itemname: "Ballet Tights",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "ballet3.jpg",
          img1: "ballet3.jpg",
          img2: "ballet3.jpg",
          img3: "ballet3.jpg",
        },
                 {
          id: 8,
          itemname: "Jazz Shoes",
          itemdesc: "Lorem ipsum dolor sit amet, consectetur",
          bigimage: "jazz1.jpg",
          img1: "jazz1.jpg",
          img2: "jazz2.webp",
          img3: "jazz1.jpg",
        },
      ],
      gallery: [
        {
          id: 1,
          img: "gal1.jpg",
          studioname:"Studio 1"
        },
          {
          id: 2,
          img: "gal2.jpg",
            studioname:"Studio 2"
        },
          {
          id: 3,
          img: "gal3.jpg",
            studioname:"Studio 3"
        },
    
      ],
    };
  },
  mounted() {},
};
</script>
