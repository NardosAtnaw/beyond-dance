<template>
  <div class="register-body">
    <Navlink />
    <div class="social-media">
      <!-- <img class="bg-back" src="../assets/img/texture.svg" alt="" /> -->
      <div class="soc-links">
        <a href="https://www.facebook.com/beyonddancers">
          <img src="../assets/img/faceblue.svg" alt="" />
        </a>
        <a href="https://www.instagram.com/beyonddancers/">
          <img src="../assets/img/instablue.svg" alt="" />
        </a>
        <a href="https://www.youtube.com/channel/UC53ryMIGEZptZToOvmBgLWQ">
          <img src="../assets/img/youblue.svg" alt="" />
        </a>
        <a href="https://www.tiktok.com/@beyonddancestudio">
          <img src="../assets/img/tiktokblue.svg" alt="" />
        </a>
      </div>
    </div>
    <div class="register-form row-max-grid">
      <div class="container row-max-grid">
        <h1>Beyond Dance Pre-Registration Form</h1>

        <p class="small-txt">
          REGISTER YOUR CHILD TODAY! - Limited Space Available
        </p>
        <p class="small-txt">
          *Due to COVID capacity constraints registration is not fully confirmed
          until pre-registration form is completed and registration is payed in
          person*
        </p>
        <div class="separt1 row-grid">
          <div class="container">
            <div class="box"></div>
          </div>
        </div>

        <form action="" @submit.prevent="submitForm" class="full-form row-grid">
          <p>Student's Name *</p>
          <p class="red-text">{{ formErrors.student_name }}</p>
          <input
            class="input"
            v-model="form.student_name"
            required
            type="text"
            data-required
            data-error-message="First Name is required"
          />
          <p>
            Parent/Guardian Name<br />
            Required for Children Ages 18 and Under
          </p>

          <input class="input" v-model="form.parent_name" type="text" />
          <p>Student's Gender *</p>
          <p class="red-text">{{ formErrors.gender }}</p>
          <p>
            <input
              type="radio"
              class="mg-left"
              v-model="form.gender"
              value="female"
              required
            />
            Female
            <input
              type="radio"
              class="mg-left"
              v-model="form.gender"
              value="male"
              required
            />
            Male
          </p>
          <p></p>
          <p>Date of Birth</p>
          <p class="red-text">{{ formErrors.dob }}</p>
          <input class="input" v-model="form.dob" type="date" required />
          <p>Age Group *</p>
          <p>
            <input
              type="radio"
              value="3-5"
              v-model="form.age_group"
              class="mg-left"
            />
            3-5 year old
            <input
              type="radio"
              value="6-9"
              v-model="form.age_group"
              class="mg-left"
            />
            6-9 year old
          </p>

          <p></p>
          <p>
            <input
              type="radio"
              value="10-13"
              v-model="form.age_group"
              class="mg-left"
            />10-13 year old
            <input
              type="radio"
              value="14-18"
              v-model="form.age_group"
              class="mg-left"
            />14-18 year old
          </p>
          <p>
            <input
              type="radio"
              value="other"
              v-model="form.age_group"
              class="mg-left"
            />Other
          </p>
          <p>School (if applicable)</p>
          <input class="input" v-model="form.school" type="text" required />
          <p>Email Address *</p>
          <p class="red-text">{{ formErrors.email }}</p>
          <input class="input" v-model="form.email" type="text" required />
          <p>Phone Number *</p>
          <p class="red-text">{{ formErrors.phone }}</p>
          <input class="input" v-model="form.phone" type="text" />
          <p>Instagram Account (if applicable)</p>
          <input class="input" v-model="form.instagram" type="text" required />
          <p>What are you interested in? (Check all that applies) *</p>
          <p class="red-text">{{ formErrors.interest }}</p>
          <p>
            <input
              type="checkbox"
              value="children"
              v-model="form.interest"
              class="mg-left"
            />
            Children's Dance Classes (Ballet, Jazz, Hip Hop, Lyrical Etc.)
          </p>

          <p>
            <input
              type="checkbox"
              value="adult"
              v-model="form.interest"
              class="mg-left"
            />Adults Classes (Yoga, Kickboxing,Salsa, Zumba...)
          </p>
          <p>
            <input
              type="checkbox"
              value="taekwondo"
              v-model="form.interest"
              class="mg-left"
            />
            Taekwondo
            <input
              type="checkbox"
              class="mg-left"
              value="summer_camp"
              v-model="form.interest"
            />
            Summer Camp
          </p>
          <p>
            <input
              type="checkbox"
              value="birthday"
              v-model="form.interest"
              class="mg-left"
            />Birthday Parties
            <input
              type="checkbox"
              value="piano"
              v-model="form.interest"
              class="mg-left"
            />
            Private Piano Lessons
          </p>
          <p></p>
          <p>
            <input
              type="checkbox"
              value="studio_space_rental"
              v-model="form.interest"
              class="mg-left"
            />
            Studio Space Rental
            <input
              type="checkbox"
              value="job"
              v-model="form.interest"
              class="mg-left"
            />
            Job Opportunity
          </p>
          <p></p>
          <p>
            <input
              type="checkbox"
              value="other"
              v-model="form.interest"
              class="mg-left"
            />
            Other
          </p>
          <p>Dancer's Shoe Size (Euro Measurements)</p>
          <input class="input" v-model="form.shoe" type="text" />
          <p>Additional Information</p>
          <input class="input" v-model="form.add_info" type="text" /><br />
          <button type="submit" class="btn btn-thrid" @submit="submitForm">
            Submit
          </button>
        </form>
      </div>
    </div>
    <div class="big-image row-grid">
      <div class="container">
        <img src="../assets/img/Takewoado.jpg" alt="" />
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from "../components/Footer.vue";
import axios from "axios";
export default {
  name: "IndexPage",
  components: { Footer },
  data() {
    return {
      formErrors: {
        student_name: "",

        gender: "",
        dob: "",

        email: "",
        phone: "",
      },
      form: {
        student_name: "",
        parent_name: "",
        gender: "",
        dob: "",
        age_group: "",
        school: "",
        email: "",
        phone: "",
        instagram: "",
        interest: [],
        shoe: "",
        add_info: "",
      },
    };
  },
  computed: {},
  methods: {
    validateForm() {
      // [1] Check If Username Is Empty
      var status = true;
      if (!this.form.student_name) {
        this.formErrors.student_name =
          "Please complete the form. Student name must not be left blank.";
        status = false;
      }
      if (!this.form.gender) {
        this.formErrors.gender =
          "Please complete the form. Gender must not be left blank.";
        status = false;
      }

      if (!this.form.dob) {
        this.formErrors.dob =
          "Please complete the form. Date of Birth must not be left blank.";
        status = false;
      }
      if (!this.form.email) {
        this.formErrors.email =
          "Please complete the form. Email must not be left blank.";
        status = false;
      }

      if (!this.form.phone) {
        this.formErrors.phone =
          "Please complete the form. Phone must not be left blank.";
        status = false;
      }

      // [2] Check If Subject Is Empty
      // if (!this.subject) {
      //   this.formErrors.push("Subject Cant Be Empty");
      // }

      // [3] Check If Message Is Empty
      // if (!this.message) {
      //   this.formErrors.push("Message Cant Be Empty");
      // }

      // [4] Check Username Characters Count
      // if (this.username && this.username.length > this.maxChars) {
      //   this.formErrors.push(
      //     `Username Cant Be More Than ${this.maxChars} Characters`
      //   );
      // }

      // If No Errors Return True
      // if (!this.formErrors.length) {
      //   return true;
      // }

      return status;
    },
    async submitForm(e) {
      // console.log(this.form);

      const result = await this.validateForm();
      console.log(result);
      if (result) {
        await axios
          .post("https://beyonddancers.com/admin/register", {
            form: this.form,
          })
          .then((res) => {
            console.log(res.data);
            // this.$router.push("/thankyou");
            window.location.href = "/thankyou";
          });
      } else {
        console.log(this.formErrors.student_name);
        e.preventDefault();
      }
    },
  },
};
</script>
