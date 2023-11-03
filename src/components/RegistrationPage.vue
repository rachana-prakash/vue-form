<template>
  <div class="reg-container">
    <section class="info-section">
      <h3>Unlock the future of enterprise communication today!</h3>
      <div>
        <p>Why sign-up for a free trial:</p>
        <DetailView />
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
export default {
  name: "RegistrationPage",
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
