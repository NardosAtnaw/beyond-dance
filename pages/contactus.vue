<template>
  <div>
    <Navlink />

    <div class="contact-page row-max-grid row-bottom-grid">
      <div class="container">
        <div class="contact-list">
          <div class="form row-grid">
            <h2>Get in touch with us!</h2>
            <h3 class="little-txt">
              Use the form below to get in touch with us, or click on the links
              to do so.
            </h3>
            <form action="">
              <p>Name</p>
              <input class="input" type="text" />
              <p>Email</p>
              <input class="input" type="text" />
              <p>Phone Number</p>
              <input class="input" type="text" />
              <p>Message</p>
              <input class="input" type="text" /><br />
              <button class="btn btn-purple">Submit</button>
            </form>
          </div>
          <div class="contact-info row-grid">
            <div class="contact-img">
              <img src="../assets/img/program/gal11.webp" alt="" />
            </div>

            <h2>Reach out to Us!</h2>
            <p>
              Africa Ave, Addis Ababa, Ethiopia<br /><br />

              Beyonddancers.com<br /><br />

              +251965757474<br /><br />
            </p>
            <div class="home-social-links">
              <div class="soc-links">
                <a href="https://www.facebook.com/beyonddancers">
                  <img src="../assets/img/faceblue.svg" alt="" />
                </a>
                <a href="https://www.instagram.com/beyonddancers/">
                  <img src="../assets/img/instablue.svg" alt="" />
                </a>
                <a
                  href="https://www.youtube.com/channel/UC53ryMIGEZptZToOvmBgLWQ"
                >
                  <img src="../assets/img/youblue.svg" alt="" />
                </a>
                <a href="https://www.tiktok.com/@beyonddancestudio">
                  <img src="../assets/img/tiktokblue.svg" alt="" />
                </a>
              </div>
            </div>
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

    <Footer />
  </div>
</template>

<script>
import Contactus from "../components/Contactus.vue";
export default {
  data() {
    return {};
  },
  mounted() {},
  components: { Contactus },
};
</script>
