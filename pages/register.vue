<template>
  <div class="register-body">
    <Navlink />
    <div class="social-media">
      <img class="bg-back" src="../assets/img/texture.svg" alt="" />
      <div class="soc-links">
        <a href="https://www.facebook.com/beyonddancers">
          <img src="../assets/img/facebookwhite.svg" alt="" />
        </a>
        <a href="https://www.instagram.com/beyonddancers/">
          <img src="../assets/img/instawhite.svg" alt="" />
        </a>
        <a href="https://www.youtube.com/channel/UC53ryMIGEZptZToOvmBgLWQ">
          <img src="../assets/img/youtubewhite.svg" alt="" />
        </a>
        <a href="https://www.tiktok.com/@beyonddancestudio">
          <img src="../assets/img/tiktokwhite.svg" alt="" />
        </a>
      </div>
    </div>
    <div class="register-form row-max-grid">
      <div class="container row-max-grid">
        <h1>Beyond Dance Pre-Registration Form</h1>
        <p class="row-grid">
          REGISTER YOUR CHILD TODAY! - Limited Space Available
        </p>
        <p class="row-grid">
          *Due to COVID capacity constraints registration is not fully confirmed
          until pre-registration form is completed and registration is payed in
          person*
        </p>

        <form action=" " class="full-form row-max-grid">
          <p>Student's Name *</p>
          <input class="input" type="text" />
          <p>
            Parent/Guardian Name<br />
            Required for Children Ages 18 and Under
          </p>
          <input class="input" type="text" />
          <p>Student's Gender *</p>
          <p>
            <input type="radio" name="gender" value="female" class="mg-left" />
            Female
            <input type="radio" class="mg-left" name="gender" value="male" />
            Male
          </p>
          <p></p>
          <p>Date of Birth</p>
          <input class="input" type="date" />
          <p>Age Group *</p>
          <p>
            <input type="radio" class="mg-left" />
            3-5 year old <input type="radio" class="mg-left" /> 6-9 year old
          </p>

          <p></p>
          <p>
            <input type="radio" class="mg-left" />10-13 year old
            <input type="radio" class="mg-left" />14-18 year old
          </p>
          <p><input type="radio" class="mg-left" />Other</p>
          <p>School (if applicable)</p>
          <input class="input" type="text" />
          <p>Email Address *</p>
          <input class="input" type="text" />
          <p>Phone Number *</p>
          <input class="input" type="text" />
          <p>Instagram Account (if applicable)</p>
          <input class="input" type="text" />
          <p>What are you interested in? (Check all that applies) *</p>
          <p>
            <input type="checkbox" class="mg-left" /> Children's Dance Classes
            (Ballet, Jazz, Hip Hop, Lyrical Etc.)
          </p>

          <p>
            <input type="checkbox" class="mg-left" />Adults Classes (Yoga,
            Kickboxing,Salsa, Zumba...)
          </p>
          <p>
            <input type="checkbox" class="mg-left" /> Taekwondo<input
              type="checkbox"
              class="mg-left"
            />
            Summer Camp
          </p>
          <p>
            <input type="checkbox" class="mg-left" />Birthday Parties
            <input type="checkbox" class="mg-left" /> Private Piano Lessons
          </p>
          <p></p>
          <p>
            <input type="checkbox" class="mg-left" /> Studio Space Rental
            <input type="checkbox" class="mg-left" /> Job Opportunity
          </p>
          <p></p>
          <p><input type="checkbox" class="mg-left" /> Other</p>
          <p>Dancer's Shoe Size (Euro Measurements)</p>
          <input class="input" type="text" />
          <p>Additional Information</p>
          <input class="input" type="text" />
        </form>
        <button class="btn btn-thrid">Submit</button>
      </div>
    </div>
    <div class="big-image row-grid">
      <img src="../assets/img/showcase 2.jpg" alt="" />
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from "../components/Footer.vue";
export default {
  name: "IndexPage",
  components: { Footer },
};
</script>
