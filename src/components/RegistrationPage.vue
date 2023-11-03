<template>
  <div class="reg-container">
    <section class="info-section">
      <div class="logo-wrapper">
        <img class="logo" src="../assets/prezent-logo.svg" />
      </div>
      <h3 class="main-title">
        Unlock the future of enterprise communication today!
      </h3>
      <div>
        <p class="sub-title">Why sign-up for a free trial:</p>
        <div class="detail-container">
          <template v-for="item in detailList" :key="item.id">
            <DetailView
              :title="item.title"
              :description="item.description"
              :imgSrc="item.imgSrc"
            />
          </template>
        </div>
      </div>
      <TestimonialView
        :testimonial="testimonialData.quote"
        :witness="testimonialData.wintess"
        :designation="testimonialData.designation"
      />
    </section>
    <section class="form-section">
      <h3 class="form-title">
        <strong>
          Join Prezent and transform the way your team Collaborates, Creates,
          and Presents.
        </strong>
      </h3>
      <RegistrationForm />
    </section>
  </div>
</template>

<script>
import RegistrationForm from "./RegistrationForm.vue";
import DetailView from "./DetailView.vue";
import TestimonialView from "./TestimonialView.vue";
import ai from "../assets/ai.svg";
import learning from "../assets/learning.svg";
import cost from "../assets/cost.svg";
import security from "../assets/security.svg";
export default {
  name: "RegistrationPage",
  data() {
    return {
      detailList: [
        {
          id: 1,
          title: "AI-Powered presentations",
          description:
            "Why spend hours on slides when you can have them ready in seconds? Our Generative AI crafts on-brand presentations tailored to your audience.",
          imgSrc: ai,
        },
        {
          id: 2,
          title: "On-Demand learning",
          description:
            "Level up your communication skills with our on-the-go learning modules. Know what ticks for your colleagues and bosses.",
          imgSrc: learning,
        },
        {
          id: 3,
          title: "Streamlined costs",
          description:
            "Cut down on agency expenses by up to 60% and allocate your budget where it truly matters.",
          imgSrc: cost,
        },
        {
          title: "Enterprise-Grade security",
          description:
            "Your data's safety is our top priority. We're compliant with GDPR, ISO/IEC 27001:2013, SOC 2 Type 2, and CCPA standards.",
          imgSrc: security,
        },
      ],
      testimonialData: {
        quote:
          "Prezent blew away my expectations, and made my life so much easier! You’ve uncovered the secret in our consulting firms who charge us so much for presentations and slides.",
        wintess: "Chief of Staff, Head of Business Strategy.",
        designation: "Fortune 500 company",
      },
    };
  },
  components: { RegistrationForm, DetailView, TestimonialView },
};
</script>

<style scoped>
.reg-container {
  display: flex;
  flex-direction: column-reverse;
  padding: 48px 22px 22px 22px;
}
.sub-title {
  font-size: 20px;
  font-weight: 400;
  padding: 8px 0;
}

.form-section {
  padding: 16px 0;
}
.form-title {
  font-size: 16px;
  line-height: 1.5;
}
.detail-container {
  padding-bottom: 20px;
}
.logo-wrapper {
  z-index: 99;
  position: absolute;
  top: 29px;
  bottom: auto;
  right: auto;
}
.logo {
  width: 90px;
}
@media screen and (min-width: 768px) {
  .reg-container {
    flex-direction: row;
    padding: 0;
  }
  .info-section {
    padding: 30px 30px 30px 100px;
    margin: 10px 10px 10px 20px;
    flex-basis: calc(55% - 20px);
  }
  .form-section {
    flex-basis: 45%;
    background-color: var(--blue1);
    color: white;
    padding: 60px;
    padding-top: 100px;
  }
  .main-title {
    padding-top: 24px;
    width: 300px;
  }
  .sub-title {
    color: var(--blue1);
  }
  .logo {
    width: 120px;
  }
  .logo-wrapper {
    position: static;
  }
}
</style>
