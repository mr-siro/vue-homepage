<template>
  <div class="category-wrapper" :style="containerStyle">
    <div class="left-cate" :style="imgStyle">
      <img width="85px" height="85px" alt="#" :src="image">
    </div>
    <div class="right-cate" :style="contentStyle">
      <h5 :style="{color:titleColor, textAlign:textFloat}">{{ title }}</h5>
      <p :style="{textAlign: textFloat}">{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CateFeature",
  props: {
    imgStyle: Object,
    textFloat: String,
    titleColor: String,
    image: String,
    title: String,
    contentStyle: Object,
    containerStyle: Object,
    description: String
  }
}
</script>

<style scoped>
.category-wrapper {
  display: flex;
}

p {
  max-width: 260px;
  color: #616368;
  text-align: left
}

h5 {
  font-weight: bold;
  text-align: left
}
</style>
