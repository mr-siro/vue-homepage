<template>
  <div class="get-awesome-wrapper">
    <div class="child-wrapper">
      <b-container>
        <div class="awesome-main-text">
          <h3 class="awe-title">{{ txt.awesomeTitle }}</h3>
          <p class="awe-sub">{{ txt.awesomeSub }}</p>
        </div>
        <div class="wrapper-button">
          <div class="view-button">
            <b-button class="mont-btn" :variant="variantValue.variantMon" pill @click="monthClick">Monthly</b-button>
            <b-button class="mon-btn" pill :variant="variantValue.variantAnu" @click="anuClick">Annually</b-button>
          </div>
        </div>
        <div class="main-price">
          <CardPrice
              :price="0"
              title="Business Class"
              sub-title="For small teams or office"
              description="Drag & Drop Builder 1,000's of Templates Blog Support Tools eCommerce Store"
              title-button="Start free trail"
          />
          <CardPrice
              class="pro-master"
              :price="99"
              title="Pro Master"
              sub-title="For Best opportunities"
              description="Drag & Drop Builder 1,000's of Templates Blog Support Tools eCommerce Store"
              title-button="Subscribe Now"
              bonus="Or Start 14 days trail"
          />
        </div>
      </b-container>
    </div>
  </div>
</template>

<script>
import CardPrice from "@/components/card/CardPrice";

export default {
  name: "GetAwesome",
  components: {
    CardPrice
  },

  data() {
    return {
      txt: {
        awesomeTitle: 'Get awesome features, without extra charges',
        awesomeSub: "The rise of mobile devices transforms the way we consume information entirely and the world's most elevant channels such as Facebook."
      },
      variantValue: {
        variantMon: 'primary',
        variantAnu: 'outline'
      }
    }
  },
  methods: {
    monthClick() {
      this.variantValue.variantMon = 'primary';
      this.variantValue.variantAnu = 'outline';
    },
    anuClick() {
      this.variantValue.variantAnu = 'primary';
      this.variantValue.variantMon = 'outline';
    }
  }
}
</script>

<style scoped>
.get-awesome-wrapper {
  padding-top: 6rem;
  display: flex;
  justify-content: center;
  border-bottom: 0.5px solid lightgray;
}

.awe-title {
  color: #242f51;
  font-weight: bold;
  display: inline-flex;
  max-width: 450px;
}

.awe-sub {
  color: #616368;
  display: inline-flex;
  max-width: 590px;
}

.child-wrapper {
  max-width: 680px;
}

.wrapper-button {
  border-radius: 25px;
  border: 0.5px solid lightgray;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  margin-top: 5%;
}

.view-button {
  margin: 3px;
}

.mon-btn {
  box-shadow: none !important;
}
.pro-master {
  border: 0.5px solid lightgray;
}

.main-price {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  padding-top: 2rem;
  padding-bottom: 10%;
  flex-wrap: wrap;
}
</style>
