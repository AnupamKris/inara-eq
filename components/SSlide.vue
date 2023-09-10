<template>
  <div class="slide">
    <img :src="`/ser${image}.png`" alt="aaa" />
    <div class="text" :class="positions[image % 4]">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed, accusamus!
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  text: String,
  image: Number,
  position: String,
});

let positions = ["topleft", "topright", "bottomleft", "bottomright"];
</script>

<style lang="scss" scoped>
.slide {
  height: 500px;
  width: 100vw;
  position: relative;

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .text {
    position: absolute;

    // transform: translate(0, -50%);
    color: #141414;
    font-size: 20px;
    font-weight: 500;
    text-align: center;

    width: 400px;
    height: 150px;
    margin-bottom: 40px;
    background: #ffffff;

    display: flex;
    justify-content: center;
    align-items: center;
  }

  .topleft {
    top: 0;
    left: 0;

    margin: 40px 0 0 0;
  }

  .topright {
    top: 0;
    right: 0;

    margin: 40px 0 0 0;
  }

  .bottomleft {
    bottom: 0;
    left: 0;

    margin: 0 0 40px 0;
  }

  .bottomright {
    bottom: 0;
    right: 0;

    margin: 0 0 40px 0;
  }
}
</style>
