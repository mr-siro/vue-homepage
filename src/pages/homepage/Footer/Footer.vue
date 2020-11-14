<template>
<div class="footer-wrapper">
  <b-container class="main-footer">
    <span>
      <img alt="#" :src="images.brandSecond">
    </span>
    <ul class="feature-footer-title my-5">
      <li>Home</li>
      <li>Key Features</li>
      <li>Pricing</li>
      <li>Testiminial</li>
      <li>FAQ</li>
    </ul>
    <div class="lst-icon">
      <img alt="#" class="icon-footer" :src="icons.IconFb">
      <img alt="#" class="icon-footer" :src="icons.IconTwister">
      <img alt="#" class="icon-footer" :src="icons.IconDif">
      <img alt="#" class="icon-footer" :src="icons.IconGit">
    </div>
    <p class="copyRight">{{txt.copyRight}}</p>
  </b-container>
</div>
</template>

<script>
import {Images} from "@/assets/Images";

export default {
name: "Footer",
  data() {
  return {
    images:{
      brandSecond: Images.brandSecond
    },
    icons: {
      IconFb: Images.IcFb,
      IconTwister: Images.IcTwister,
      IconDif: Images.IcDif,
      IconGit: Images.IcGit
    },
    txt: {
      copyRight: 'Copyright© Arifur Rahman Tushar 2019. All rights reserved'
    }
  }
  }
}
</script>

<style scoped>
.footer-wrapper {
  background-image: url("../../../assets/images/footer_03.png");
  background-position: top;
  background-repeat: no-repeat;
  background-size: cover;
  z-index: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
.main-footer {
  padding: 6rem 0;
}

.feature-footer-title li {
  list-style: none;
  color: #fff;
  margin-right: 3rem;
  display: inline-flex;
}

.icon-footer {
  width: 30px;
  height: 30px;
  margin: 0 0.5em;
}
.copyRight {
  font-size: 14px;
  color: #ffffff;
  margin-top: 5rem;
}
</style>
