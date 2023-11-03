<template>
  <div class="reg-container">
    <section class="info-section">
      <h3>Unlock the future of enterprise communication today!</h3>
      <div>
        <p>Why sign-up for a free trial:</p>
        <div>
          <template v-for="item in detailList" :key="item.id">
            <DetailView
              :title="item.title"
              :description="item.description"
              :imgSrc="item.imgSrc"
            />
          </template>
        </div>
      </div>
      <TestimonialView />
    </section>
    <section class="form-section">
      <h3>
        Join Prezent and transform the way your team Collaborates, Creates, and
        Presents.
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
    };
  },
  components: { RegistrationForm, DetailView, TestimonialView },
};
</script>

<style scoped>
.reg-container {
  display: flex;
  flex-direction: column-reverse;
}
@media screen and (min-width: 768px) {
  .reg-container {
    flex-direction: row;
  }
}
</style>
