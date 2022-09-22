<template>
  <header>
    <nav class="home-nav">
      <div class="container">
        <div class="logo">
          <nuxt-link to="/">
            <!-- <div>
              <img class="bottom" src="@/assets/img/logoballet.svg" alt="" />
              <img class="top" src="@/assets/img/takwalogo.svg" alt="" /> -->
            <!-- <img class="mid" src="../assets/img/gymlogo.svg" alt="" /> -->
            <!--
              <img class="mid2" src="../assets/img/hiphoplogo.svg" alt="" /> -->
            <!-- </div> -->
            <div class="bg-container">
              <div class="bg-block active">
                <img src="../assets/img/logo1.svg" alt="" />
              </div>
              <div class="bg-block">
                <img class="mid2" src="../assets/img/logo2.svg" alt="" />
              </div>
              <div class="bg-block">
                <img src="../assets/img/logo3.svg" />
              </div>
              <div class="bg-block">
                <img src="../assets/img/logo4.svg" />
              </div>
              <div class="bg-block">
                <img src="../assets/img/logo5.svg" />
              </div>
              <div class="bg-block">
                <img src="../assets/img/logo6.svg" />
              </div>
            </div>
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
                <li>
                  <nuxt-link to="/events">Events</nuxt-link>
                  <ul class="dropdown">
                    <li><nuxt-link to="/kidsevent">Kids Event</nuxt-link></li>
                    <li>
                      <nuxt-link to="/adultevent">Adult Events</nuxt-link>
                    </li>
                    <li>
                      <nuxt-link to="/adultclass">Adult Classes</nuxt-link>
                    </li>
                    <li>
                      <nuxt-link to="/wedding">Wedding Packages</nuxt-link>
                    </li>
                  </ul>
                </li>
                <li><nuxt-link to="/contactus">Contact Us</nuxt-link></li>
                <li>
                  <nuxt-link to="/register">Register Now </nuxt-link>
                </li>
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
            <li>
              <nuxt-link to="/events">Events</nuxt-link>
              <ul class="dropdown">
                <li><nuxt-link to="/kidsevent">Kids Event</nuxt-link></li>
                <li>
                  <nuxt-link to="/adultevent">Adult Events</nuxt-link>
                </li>
                <li>
                  <nuxt-link to="/adultclass">Adult Classes</nuxt-link>
                </li>
                <li>
                  <nuxt-link to="/wedding">Wedding Packages</nuxt-link>
                </li>
              </ul>
            </li>
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
  mounted() {
    $(document).ready(function () {
      //save boolean
      var pause = false;
      //save items that with number
      var item = $(".select-item");
      //save blocks
      var block = $(".bg-block");
      //variable for counter
      var k = 0;

      //interval function works only when pause is false
      setInterval(function () {
        if (!pause) {
          var $this = item.eq(k);

          if (item.hasClass("active")) {
            item.removeClass("active");
          }
          block.removeClass("active").eq(k).addClass("active");
          $this.addClass("active");
          //increase k every 1.5 sec
          k++;
          //if k more then number of blocks on page
          if (k >= block.length) {
            //rewrite variable to start over
            k = 0;
          }
        }
        //every 1.5 sec
      }, 1500);

      item.hover(
        function () {
          //remove active class from all except this
          $(this).siblings().removeClass("active");
          $(this).addClass("active");
          //remove active class from all
          block.removeClass("active");
          //add active class to block item which is accounted as index cliked item
          block.eq($(this).index()).addClass("active");
          //on hover stop interval function
          pause = true;
        },
        function () {
          //when hover event ends, start interval function
          pause = false;
        }
      );
    });
  },
};
</script>
