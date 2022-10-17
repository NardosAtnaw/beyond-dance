<template>
  <div>
    <Navlink />
    <section class="login-main-wrapper">
      <div class="container">
        <div class="login-process">
          <div class="login-main-container">
            <div class="thankyou-wrapper">
              <h1>
                <img
                  src="http://montco.happeningmag.com/wp-content/uploads/2014/11/thankyou.png"
                  alt="thanks"
                />
              </h1>
              <p>for Pre-registering, we will get in touch with you soon...</p>
              <button class="btn btn-purple">
                <a href="/">Back to Home</a>
              </button>
              <div class="clr"></div>
            </div>
            <div class="clr"></div>
          </div>
        </div>
        <div class="clr"></div>
      </div>
    </section>
    <Footer />
  </div>
</template>

<script>
import Footer from "../components/Footer.vue";
export default {
  components: { Footer },
};
</script>
