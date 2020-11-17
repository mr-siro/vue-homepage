<template>
  <div class="header-wrapper">
    <div class="mt-5 flex-column d-flex justify-content-end">
      <b-container>
        <b-navbar toggleable="lg" type="light">
          <b-navbar-brand href="#">
            <img alt="brand" width="145" height="50" :src="image.brand">
          </b-navbar-brand>
          <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
          <b-collapse id="nav-collapse" is-nav>
            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
              <b-nav-item href="#">Home</b-nav-item>
              <b-nav-item href="#">Key Features</b-nav-item>
              <b-nav-item href="#">Pricing</b-nav-item>
              <b-nav-item href="#">Testiminial</b-nav-item>
              <b-nav-item href="#">FAQ</b-nav-item>
              <b-button class="btn-try ml-2" pill variant="primary">Try for free</b-button>
            </b-navbar-nav>
          </b-collapse>
        </b-navbar>
        <b-row class="align-items-center mx-4">
          <div class="col-md-7">
            <div class="left-header">
              <img style="max-width: 100%; float: left" :src="image.editChoice" alt="#">
              <div class="text-header">
                <h2>{{ text.h1 }}</h2>
                <p class="sub-title">{{ text.subTitle }}</p>
              </div>
              <b-row class="d-flex align-items-center">
                <b-button class="btn-try mx-3" pill variant="primary">Try for free</b-button>
                <b-link class="link-video">Watch demo video</b-link>
              </b-row>
            </div>
          </div>
          <div class="col-md-5">
            <div class="right-header">
              <img width="100%" height="auto" alt="#" :src="image.phone">
            </div>
          </div>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<script>
import {Images} from "@/assets/Images";

export default {
  name: "Header",
  data() {
    return {
      image: {
        brand: Images.brand,
        phone: Images.phone,
        editChoice: Images.editChoice,
        buildDing: Images.buildDing
      },
      text: {
        h1: 'Best app for your modern lifestyle',
        subTitle: 'Increase productivity with a simple to-do app. app for managing your personal budgets.'
      }
    }
  }
}
</script>

<style>

.left-header {
  max-width: 55%;
  margin-left: 3rem;
}

.right-header {
  margin-left: 2rem;
}

.btn-try {
  background-color: #2500f9;
}

h2 {
  color: #242f51;
  text-align: left;
  font-weight: bold;
}

li.nav-item {
  margin-right: 2rem;
}

.navbar-light .navbar-nav .nav-link {
  color: black;
}

.sub-title {
  color: #616368;
  text-align: left;
}

.link-video {
  color: #2500f9;
  font-size: 16px;
}

.text-header {
  padding-top: 15%;
}

.bottom-header {
  margin: 0;
  padding: 0;
  z-index: -1;
  position: absolute;
}

.header-wrapper {
  background-image: url("../../assets/images/header_01.png");
  background-position: center bottom;
  background-repeat: repeat;
  background-size: cover;
  z-index: 1;
}
</style>
