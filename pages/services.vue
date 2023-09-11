<template>
  <div class="services">
    <h3>Services</h3>

    <carousel :items-to-show="1" :autoplay="2000">
      <slide v-for="slide in 5" :key="slide">
        <SSlide position="topleft" :image="slide" />
      </slide>

      <template #addons>
        <navigation />
        <pagination />
      </template>
    </carousel>

    <h3>Our Offerings</h3>

    <div class="accordion">
      <div class="service" :class="currentAccordion == 0 ? 'expanded' : ''">
        <div class="title" @click="currentAccordion = 0">
          <p>Digital</p>
          <Icon name="eva:arrow-ios-downward-outline" />
        </div>
        <div class="content">
          <p>Digital Marketing</p>
          <p>Web Development</p>
          <p>App Development</p>
          <p>SEO</p>
          <p>Software Design</p>
        </div>
      </div>
      <div class="service" :class="currentAccordion == 1 ? 'expanded' : ''">
        <div class="title" @click="currentAccordion = 1">
          <p>Assets</p>
          <Icon name="eva:arrow-ios-downward-outline" />
        </div>
        <div class="content">
          <p>Real Estate</p>
          <p>Stocks</p>
          <p>Commodities</p>
          <p>Forex</p>
          <p>ETFs</p>
        </div>
      </div>
      <div class="service" :class="currentAccordion == 2 ? 'expanded' : ''">
        <div class="title" @click="currentAccordion = 2">
          <p>Sales</p>
          <Icon name="eva:arrow-ios-downward-outline" />
        </div>
        <div class="content">
          <p>Gold</p>
          <p>Iron</p>
          <p>Steel</p>
          <p>Aluminum</p>
          <p>Precious Metals</p>
        </div>
      </div>
      <div class="service" :class="currentAccordion == 3 ? 'expanded' : ''">
        <div class="title" @click="currentAccordion = 3">
          <p>Trrading</p>
          <Icon name="eva:arrow-ios-downward-outline" />
        </div>
        <div class="content">
          <p>Gold</p>
          <p>Srap Metal</p>
          <p>General</p>
          <p>Metal Waste</p>
          <p>Electronic Money</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const currentAccordion = ref(null);
</script>

<style lang="scss" scoped>
* {
  margin: 0;
  padding: 0;
}

.services {
  width: 100%;
  background: #141414;
  padding: 10px 0;
  color: #ffffff;

  display: flex;
  flex-direction: column;
  // justify-content: center;
  align-items: center;

  h3 {
    width: 90%;
    font-size: 24px;
    font-weight: 500;
    margin-bottom: 10px;
    // text-transform: uppercase;

    padding: 30px 10px;
  }

  .carousel {
    .carousel__slide {
      width: 80%;
    }
  }

  .row {
    margin-top: 30px;
    width: 80%;
    max-width: 600px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .set {
      width: 30%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;

      .icon {
        width: 60px;
        height: 60px;
        border-radius: 50%;
        background: #d4a742;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: 20px;
        svg {
          width: 30px;
          height: 30px;
          color: #ffffff;
        }
      }

      h4 {
        font-size: 14px;
        font-weight: 500;
        margin-bottom: 10px;
        text-transform: uppercase;
      }

      p {
        font-size: 12px;
        font-weight: 400;
        color: #bebebe;
      }
    }
  }

  .accordion {
    width: 85%;
    // max-width: 600px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    padding-bottom: 40px;

    .service {
      width: 100%;
      height: 50px;
      transition: 0.3s;
      border-bottom: 2px solid #494949;
      .title {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        font-size: 18px;
        p {
          padding: 10px 0;
        }
        .icon {
          width: 24px;
          height: 24px;
          color: #c2c2c2;
          transition: 0.3s;
        }
      }

      .content {
        width: 100%;
        height: 0;
        overflow: hidden;
        transition: 0.3s;
        p {
          padding: 10px 0;
          font-size: 14px;
          font-weight: 200;
          color: #bebebe;
          text-align: left;
        }
      }
    }

    .expanded {
      height: 260px;
      .title {
        p {
          color: #d4a742;
        }
        .icon {
          transform: rotate(180deg);
        }
      }

      .content {
        height: 350px;
      }
    }
  }
}
</style>
