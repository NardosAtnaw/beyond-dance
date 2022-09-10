<template>
  <header>
    <nav class="home-nav">
      <div class="container">
        <div class="logo">
          <nuxt-link to="/">
            <img src="@/assets/img/logopng.png" alt="" />
          </nuxt-link>
        </div>

        <div class="mobile-link">
          <nav role="navigation">
            <div id="menuToggle">
              <input type="checkbox" />
              <span></span>
              <span></span>
              <span></span>

              <ul id="menu" class="ul-links1">
                <li><nuxt-link to="/">Home</nuxt-link></li>
                <li><nuxt-link to="/dancestudio">Dance Studio</nuxt-link></li>
                <li><nuxt-link to="/program">Programs</nuxt-link></li>
                <li>
                  <nuxt-link to="/performance"
                    >Performance Information and Videos</nuxt-link
                  >
                </li>
                <li><nuxt-link to="/events">Events</nuxt-link></li>
                <li><nuxt-link to="/contactus">Contact Us</nuxt-link></li>
              </ul>
            </div>
          </nav>
         
        </div>
        <div class="links">
          <ul class="ul-links">
            <li><nuxt-link to="/">Home</nuxt-link></li>
            <li><nuxt-link to="/dancestudio">Dance Studio</nuxt-link></li>
            <li><nuxt-link to="/program">Programs</nuxt-link></li>
            <li>
              <nuxt-link to="/performance"
                >Performance Information and Videos</nuxt-link
              >
            </li>
            <li><nuxt-link to="/events">Events</nuxt-link></li>
            <li><nuxt-link to="/contactus">Contact Us</nuxt-link></li>
            <li>
              <nuxt-link to="/register"
                ><span class="box-form">Register Now</span>
              </nuxt-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  el: "#app",
  data: {
    isOpen: false,
  },
};
</script>
