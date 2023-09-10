<template>
  <nav>
    <div class="logo">
      <img src="/logo.png" alt="" />
      <p>INARA EQUINIX</p>
    </div>
    <div class="nav-items">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/services">Services</router-link>
      <router-link to="/news">News</router-link>
      <router-link to="/contact">Contact</router-link>
    </div>
  </nav>
</template>

<script setup></script>

<style lang="scss" scoped>
nav {
  height: 70px;
  background: #141414;

  display: flex;
  justify-content: space-between;
  align-items: center;

  color: #ffffff;
  border-bottom: 2px solid #d4a742;

  .logo {
    width: 100px;
    height: 100%;

    display: flex;
    justify-content: flex-start;
    align-items: center;

    flex-direction: column;
    padding-top: 10px;

    img {
      height: 60%;
    }

    p {
      font-size: 9px;
    }
  }

  .nav-items {
    width: 40%;
    height: 100%;

    display: flex;
    justify-content: space-around;
    align-items: center;

    a {
      text-decoration: none;
      color: #ffffff;
    }

    .router-link-active {
      color: #d4a742;
    }
  }
}
</style>
