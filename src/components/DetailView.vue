<template>
  <div class="detail-container">
    <div class="img-container">
      <div class="img-wrapper">
        <img :src="imgSrc" />
      </div>
    </div>

    <div class="text-container">
      <p class="title">{{ title }}</p>
      <p class="description">{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "DetailView",
  props: ["title", "description", "imgSrc"],
};
</script>

<style scoped>
.detail-container {
  display: flex;
}
.img-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;

  background-color: white;
  border: solid 2px var(--steel-blue);
  border-radius: 20%;
}
.img-container {
  margin: 4px;
  padding: 4px;
}
img {
  height: 36px;
  width: 36px;
  padding: 10px;
}
.text-container {
  margin: 4px;
  display: flex;
  flex-direction: column;
}
.title {
  font-weight: 400;
  font-size: 18px;
  padding: 4px;
}
.description {
  font-size: 16px;
  font-weight: 300;
  padding: 4px;
}
</style>
