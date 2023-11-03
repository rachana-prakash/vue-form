<template>
  <div class="container">
    <div class="img-container">
      <img :src="quote" />
    </div>
    <div class="quote-container">
      <q>{{ testimonial }}</q>
    </div>
    <div class="signature">
      <p class="witness">{{ witness }}</p>
      <p class="designation">{{ designation }}</p>
    </div>
  </div>
</template>

<script>
import quote from "../assets/quote.svg";
export default {
  name: "TestimonialView",
  props: ["testimonial", "witness", "designation"],
  data() {
    return { quote };
  },
};
</script>

<style scoped>
.container {
  background-color: var(--blue1);
  border-radius: 10px;
  color: white;
  padding: 32px;
}
.img-container {
  display: flex;
  justify-content: flex-end;
}
img {
  height: 28px;
  opacity: 0.65;
}
.quote-container {
  font-size: 16px;
  padding-bottom: 10px;
  font-weight: 400;
}
.signature {
  padding-top: 10px;
  font-size: 15px;
}
.witness {
  padding-bottom: 8px;
  font-size: 14px;
}
@media screen and (min-width: 768px) {
  .container {
    background-color: var(--grey1);
    color: black;
    padding-top: 16px;
  }
  .quote {
    font-size: 18px;
  }
}
</style>
