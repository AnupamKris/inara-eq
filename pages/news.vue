<template>
  <div class="news">
    <div class="header">
      <h1>News And Events</h1>
      <img src="/news.jpg" alt="" />
    </div>
    <div class="charts">
      <Chart id="c1" />
      <Chart2 id="c2" />
    </div>
    <div class="charts">
      <Chart3 id="c3" />
    </div>
    <div class="main-news">
      <img src="/ser3.png" alt="" />
      <div class="text">
        <h3>Investment in Company</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Aspernatur
          quae aperiam rem sit, pariatur quo iure odit! Amet, officiis
          necessitatibus.
        </p>
        <span>Read More</span>
      </div>
    </div>
    <div class="ns">
      <NewsCard />
      <NewsCard />
      <NewsCard />
      <NewsCard />
      <NewsCard />
      <NewsCard />
    </div>
  </div>
</template>

<script setup>
onMounted(() => {
  document.getElementById("__nuxt").scrollTo(0, 0);
});
</script>

<style lang="scss" scoped>
.news {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 100%;

  .header {
    width: 100%;
    height: 400px;
    background: #141414;
    color: #d4a742;
    font-size: 28px;
    font-weight: 500;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      position: absolute;
      top: 0;
      left: 0;
      filter: brightness(0.3);
    }
    h1 {
      z-index: 1;
      color: #d4a742;
      font-size: 40px;
      font-weight: 500;
      text-align: center;
    }
  }

  .charts {
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin-top: 30px;
    flex-direction: column;
  }
  .ns {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;

    width: 100%;

    background: #141414;
  }

  .main-news {
    display: flex;
    justify-content: center;
    align-items: center;
    // flex-direction: column;
    width: 100%;
    height: 600px;
    padding: 30px 20px;
    background: #141414;

    img {
      width: 58%;
      height: 100%;
      object-fit: cover;
    }

    .text {
      width: 30%;
      height: 100%;
      background: #1a1a1a;
      padding: 20px 10px;
      display: flex;
      justify-content: flex-start;
      align-items: center;
      flex-direction: column;

      h3 {
        font-size: 24px;
        font-weight: 500;
        margin-bottom: 10px;
        // text-transform: uppercase;
        padding: 10px 10px;
        width: 100%;
        color: #d4a742;
      }

      p {
        font-size: 14px;
        color: #ffffff;
        width: 100%;
        padding: 0px 10px;
      }

      span {
        font-size: 14px;
        color: #d4a742;
        width: 100%;
        padding: 0px 10px;
        margin-top: 10px;
      }
    }
  }
}

@media only screen and (max-width: 768px) {
  .news {
    .charts {
      flex-direction: column;
    }
    .header {
      height: 200px;
      h1 {
        font-size: 24px;
      }
    }
    .main-news {
      flex-direction: column;
      height: auto;
      img {
        width: 100%;
        height: 300px;
      }
      .text {
        width: 100%;
        height: auto;
        padding: 10px 10px;
        h3 {
          font-size: 18px;
        }
        p {
          font-size: 12px;
        }
        span {
          font-size: 12px;
        }
      }
    }

    .ns {
      width: 100%;
      height: auto;

      .news-card {
        width: 100%;
        height: auto;
      }
    }
  }
}
</style>
