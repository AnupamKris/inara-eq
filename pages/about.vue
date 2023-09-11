<template>
  <div class="about">
    <div class="main">
      <h2>About Us</h2>
      <p>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sunt autem
        pariatur odio alias iste voluptatum voluptates quibusdam, repellat vel
        eaque.
      </p>
    </div>
    <div class="mission">
      <div class="col">
        <h3>Our Mission</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam
          voluptatum, voluptate, quibusdam, quia voluptas quod dolorum
          voluptatibus quos quas quidem voluptatem. Quisquam voluptatum,
          voluptate, quibusdam, quia voluptas quod dolorum voluptatibus quos
          quas quidem voluptatem.
        </p>
      </div>
      <div class="col">
        <div class="row">
          <img src="/off1.jpg" alt="" />
          <img src="/mis1.jpg" alt="" />
        </div>
        <div class="row-f">
          <img src="/off1.jpg" alt="" />
        </div>
      </div>
    </div>
    <div class="team">
      <h3>Our Leaders</h3>
      <div class="row">
        <div class="member">
          <img src="/off1.jpg" alt="" />
          <h4>John Doe</h4>
          <p>CEO</p>
        </div>
        <div class="member">
          <img src="/off1.jpg" alt="" />
          <h4>John Doe</h4>
          <p>CTO</p>
        </div>
        <div class="member">
          <img src="/off1.jpg" alt="" />
          <h4>John Doe</h4>
          <p>COO</p>
        </div>
        <div class="member">
          <img src="/off1.jpg" alt="" />
          <h4>John Doe</h4>
          <p>CFO</p>
        </div>
      </div>
    </div>
    <div class="clients">
      <h3>Our Clients</h3>
      <div class="row">
        <div class="tiles"></div>
        <div class="tiles"></div>
        <div class="tiles"></div>
        <div class="tiles"></div>
        <div class="tiles"></div>
        <div class="tiles"></div>
        <div class="tiles"></div>
        <div class="tiles"></div>
        <div class="tiles"></div>
        <div class="tiles"></div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.about {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;

  .main {
    height: 500px;
    width: 100%;
    background: #141414;

    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;

    h2 {
      color: #d4a742;
      font-size: 40px;
      font-weight: 500;
      text-align: center;
      //   padding: 100px 0;
    }
    p {
      width: 60%;
      max-width: 600px;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      font-weight: 300;
      color: #d4d4d4;
    }
  }

  .mission {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #d3d3d3;
    padding-bottom: 20px;
    padding: 50px 5%;

    .col {
      width: 45%;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;

      h3 {
        font-size: 24px;
        font-weight: 500;
        margin-bottom: 10px;
        // text-transform: uppercase;
        padding: 10px 10px;
        width: 100%;
        color: #8d670e;
      }

      p {
        font-size: 16px;
        font-weight: 300;
        color: #141414;
        width: 100%;
        padding: 0px 10px;
      }

      .row {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-top: 10px;
        width: 90%;
        img {
          width: 50%;

          height: 200px;
          object-fit: cover;
          padding: 10px;
        }
      }
      .row-f {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: 10px;
        width: 90%;
        img {
          width: 100%;
          height: 200px;
          object-fit: cover;
          padding: 0 10px;
        }
      }
    }
  }

  .team {
    width: 100%;
    // height: 450px;
    background: #141414;

    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;

    padding: 60px 0;
    h3 {
      font-size: 24px;
      font-weight: 500;
      margin-bottom: 10px;
      // text-transform: uppercase;
      padding: 10px 10px;
      width: 90%;
      color: #d4a742;
    }

    .row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 10px;
      width: 90%;
      .member {
        width: 20%;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        img {
          width: 100%;
          height: 300px;
          object-fit: cover;
          padding: 10px;
        }
        h4 {
          font-size: 16px;
          font-weight: 500;
          margin-bottom: 10px;
          // text-transform: uppercase;
          color: #ffffff;
        }
        p {
          font-size: 14px;
          font-weight: 300;
          color: #ffffff;
        }
      }
    }
  }
  .clients {
    width: 100%;
    height: 600px;
    background: #d3d3d3;

    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    h3 {
      font-size: 24px;
      font-weight: 500;
      margin-bottom: 10px;
      // text-transform: uppercase;
      padding: 10px 10px;
      width: 90%;
      color: #8d670e;
    }

    .row {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      justify-content: center;
      gap: 20px;
      width: 90%;
      .tiles {
        width: 100%;
        height: 150px;
        background: #ffffff;
      }
    }
  }
}

@media screen and (max-width: 600px) {
  .mission {
    flex-direction: column;
    .col {
      width: 100% !important;
      margin-bottom: 20px;
      text-align: center;
    }
  }

  .team {
    .row {
      flex-direction: column;
      width: 100%;
      .member {
        margin-bottom: 20px;
        width: 100% !important;
        img {
          width: 90% !important;
          border-radius: 10px;
        }
      }
    }
  }

  .about {
    .clients {
      height: auto;
      padding: 30px 0;
      .row {
        grid-template-columns: repeat(2, 1fr);
        .tiles {
          height: 200px;
        }
      }
    }
  }
}
</style>
