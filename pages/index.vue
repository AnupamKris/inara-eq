<template>
  <div class="main-img">
    <div class="static">Your Assets, Our Strategy, Your Success.</div>
    <div class="slides">
      <carousel :items-to-show="1" :autoplay="2000" :wrap-around="true">
        <slide key="1">
          <div class="carousel__item">
            <img src="/main.jpg" alt="" />
          </div>
        </slide>
        <slide key="2">
          <div class="carousel__item">
            <img src="/img2.jpg" alt="" />
          </div>
        </slide>
        <template #addons>
          <Navigation />
          <Pagination />
        </template>
      </carousel>
    </div>
  </div>
  <div class="news">
    <h2>Investment views and financial market data</h2>
    <div class="cards">
      <div class="col">
        <IvCard name="DAX" value="15891.93" place="Fankfurt" percent="-0.24%" />
        <IvCard name="DAX" value="15891.93" place="Fankfurt" percent="-0.24%" />
      </div>
      <div class="col">
        <IvCard name="DAX" value="15891.93" place="Fankfurt" percent="-0.24%" />
        <IvCard name="DAX" value="15891.93" place="Fankfurt" percent="-0.24%" />
      </div>
      <div class="col">
        <IvCard name="DAX" value="15891.93" place="Fankfurt" percent="-0.24%" />
        <IvCard name="DAX" value="15891.93" place="Fankfurt" percent="-0.24%" />
      </div>
      <div class="col">
        <IvCard name="DAX" value="15891.93" place="Fankfurt" percent="-0.24%" />
        <IvCard name="DAX" value="15891.93" place="Fankfurt" percent="-0.24%" />
      </div>
    </div>
  </div>
  <div class="why">
    <h2>Why Choose Us?</h2>
    <div class="feats">
      <div class="feat">
        <Icon name="ri:coupon-3-fill" />
        <h3>Lorem ipsum dolor sit amet.</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse, iusto.
        </p>
      </div>
      <div class="feat">
        <Icon name="ri:coupon-fill" />
        <h3>Lorem ipsum dolor sit amet.</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse, iusto.
        </p>
      </div>
      <div class="feat">
        <Icon name="fluent:money-20-filled" />
        <h3>Lorem ipsum dolor sit amet.</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse, iusto.
        </p>
      </div>
    </div>
  </div>
  <div class="offerings">
    <h2>Our Offerings?</h2>
    <div class="row">
      <div class="text">
        <p>Spending & Saving</p>
        <h2>Investing for a better future</h2>
        <span
          >Fidelity cash management products help you spend and save smarter so
          you can reach your goals.</span
        >
      </div>
      <div class="img">
        <img src="/off1.jpg" alt="" />
      </div>
    </div>
    <div class="row">
      <div class="img">
        <img src="/off2.jpg" alt="" />
      </div>
      <div class="text">
        <p>Trading & Investing</p>
        <h2>Investing for a better future</h2>
        <span
          >Whether you are an active trader or investing in the future, we can
          help you reach your goals.</span
        >
      </div>
    </div>
    <div class="row">
      <div class="text">
        <p>Wholesale Purchase</p>
        <h2>Get things for most economic value</h2>
        <span
          >Whether you are an active trader or investing in the future, we can
          help you reach your goals.</span
        >
      </div>
      <div class="img">
        <img src="/off3.jpg" alt="" />
      </div>
    </div>
  </div>
  <div class="newsletter">
    <h2>Subscribe to our Newsletter</h2>
    <div class="form">
      <input type="text" placeholder="Enter your email" />
      <button>Subscribe</button>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.main-img {
  width: 100%;
  height: 650px;
  overflow: hidden;
  //   object-fit: cover;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;

  .static {
    width: 350px;
    height: 100%;

    top: 0;
    background: #1f1f1f;
    position: relative;
    z-index: 2;

    font-size: 50px;
    font-weight: 700;
    color: #ffffff;

    display: flex;
    // justify-content: center;
    align-items: center;
    text-align: left;
    padding-left: 10px;

    &::after {
      content: "";
      width: 100px;
      height: 100%;
      background: #1f1f1f;
      position: absolute;
      top: 0;
      right: -60px;
      transform: skew(-7deg);
      z-index: 2;
    }
  }

  .slides {
    width: calc(100% - 300px);
    height: 100%;
    position: relative;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      position: absolute;
      top: 0;
      z-index: 0;
    }
  }

  .carousel {
    height: 100%;
    width: 100%;
    position: relative;
    .carousel__viewport,
    .carousel__item,
    .carousel__track,
    .carousel__slide {
      height: 100%;
      width: 100%;
    }
  }

  .carousel__item {
    min-height: 630px;
    width: 100%;
    height: 100%;
    background-color: var(--vc-clr-primary);
    color: var(--vc-clr-white);
    font-size: 20px;
    border-radius: 8px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .carousel__slide {
    padding: 10px;
  }

  .carousel__prev,
  .carousel__next {
    box-sizing: content-box;
    border: 5px solid white;
    // border-radius: 50%;
  }

  .carousel__prev {
    z-index: 5;
  }

  .carousel__pagination {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
    z-index: 3;
    bottom: 10px;
    left: 50%;
    position: absolute;
    .carousel__pagination-item {
      .carousel__pagination-button {
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background: #ffffff;
        margin: 0 5px;
        cursor: pointer;
        &::after {
          background-color: #ffffff;
        }
      }
    }
  }
}

.news {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  margin: 70px 0;

  h2 {
    width: 85%;
    font-size: 24px;
    font-weight: 500;
    color: #1f1f1f;
    margin-bottom: 20px;
  }

  .cards {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 85%;
    .col {
      min-width: 250px;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      // display: flex;
      // justify-content: space-between;
      // align-items: center;
      &:nth-child(1) {
        align-items: flex-start;
      }
      &:nth-child(4) {
        align-items: flex-end;
      }
    }
  }
}

.why {
  height: 550px;
  background: #1f1f1f;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  padding: 30px 0;
  padding-bottom: 40px;

  h2 {
    width: 85%;
    font-size: 24px;
    font-weight: 500;
    color: #ffffff;
    margin-bottom: 20px;
  }
  .feats {
    width: 80%;
    display: flex;
    justify-content: space-around;
    align-items: center;
    .feat {
      height: 300px;
      width: 300px;
      border-radius: 50%;

      background: #303030;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      .icon {
        width: 70px;
        height: 70px;
        border-radius: 50%;
        // background: #ffffff;
        color: #ffffff;
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 0 auto;
        margin-top: 20px;
      }

      h3 {
        width: 90%;
        font-size: 20px;
        font-weight: 500;
        color: #d4a742;

        text-align: center;
      }

      p {
        width: 70%;
        font-size: 14px;
        font-weight: 300;
        color: #b4b4b4;
        text-align: center;
      }
    }
  }
}

.offerings {
  width: 100%;
  height: 1150px;
  padding: 50px 0;
  background: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  h2 {
    width: 85%;
    font-size: 24px;
    font-weight: 500;
    color: #1f1f1f;
    margin-bottom: 20px;
  }
  .row {
    width: 80%;
    height: 300px;
    margin: 10px 0;
    display: flex;
    justify-content: center;
    align-items: center;

    .text {
      width: 50%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      padding: 0 20px;
      p {
        width: 100%;
        font-size: 14px;
        font-weight: 500;
        color: #d4a742;
        // text-align: center;
        margin-bottom: 10px;
      }
      h2 {
        width: 100%;
        font-size: 24px;
        font-weight: 500;
        color: #1f1f1f;
        margin-bottom: 10px;
      }
      span {
        width: 100%;
        font-size: 16px;
        font-weight: 300;
        color: #616161;
        // text-align: center;
      }
    }
    .img {
      width: 50%;
      height: 100%;
      border-radius: 20px;
      overflow: hidden;
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
  }
}

.newsletter {
  width: 100%;
  height: 300px;
  background: #1f1f1f;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  h2 {
    width: 85%;
    font-size: 24px;
    font-weight: 500;
    color: #ffffff;
    margin-bottom: 20px;
  }

  .form {
    width: 85%;
    height: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    input {
      width: 70%;
      height: 100%;
      border: none;
      outline: none;
      padding: 0 20px;
      border-radius: 5px 0 0 5px;
      font-size: 14px;
      font-weight: 300;
      color: #616161;
    }
    button {
      width: 30%;
      height: 100%;
      border: none;
      outline: none;
      border-radius: 0 5px 5px 0;
      background: #d4a742;
      color: #ffffff;
      font-size: 14px;
      font-weight: 300;
      cursor: pointer;
    }
  }
}
</style>
