<template>
  <div class="price-wrapper">
    <div class="card-price-top">
      <div class="content-top pt-5 pb-2">
        <div class="context-price">
          <h1>${{price.toString()}}</h1>
          <p class="sub-price">/ month</p>
        </div>
        <div class="context-title">
          <h5>{{title}}</h5>
          <p>{{subTitle}}</p>
        </div>
      </div>
    </div>
    <div class="card-price-bottom">
      <div class="content-bottom">
        <p class="des-price">{{description}}</p>
      </div>
      <b-button style="background-color: #2500f9" pill variant="primary">{{titleButton}}</b-button>
      <p class="py-3" style="color: #2500f9">{{bonus}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardPrice",
  props: {
    price: Number,
    title: String,
    subTitle: String,
    description: String,
    titleButton: String,
    bonus:{
      type: String,
      required:false
    }
  }
}
</script>

<style scoped>
.price-wrapper {
  max-width: 315px;
  -webkit-box-shadow: -1px -1px 15px 5px #EDEDED;
  box-shadow: -1px -1px 15px 5px #EDEDED;
}

.card-price-top {
  background-color: #f9fbfc;
}

.card-price-bottom {
  background-color: #ffffff;
}

.context-price {
  display: flex;
  justify-content: center;
  align-items: baseline;
}

h1 {
  font-weight: 800;
  color: #242f51;
}

h5 {
  color: #242f51;
  font-weight: bold;
}
.sub-price {
  color: #999ca5;
  font-size: 18px;
}
.context-title p {
  color: #999ca5;
}
.des-price {
  color: #999ca5;
}

.content-bottom {
  margin: 1.5rem 4rem;
}
</style>
