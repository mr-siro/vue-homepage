<template>
  <div class="testimonial-wrapper">
    <el-container direction="vertical">
      <el-row>
        <el-col :md="12">
          <img style="max-width: 100%" alt="#" :src="images.testier">
        </el-col>
        <el-col :md="10">
          <div class="right-test">
            <div class="context-test">
              <h3>{{ txt.titleTest }}</h3>
              <p class="py-3">{{ txt.subTest }}</p>
            </div>
            <el-rate
                v-model="valueRate"
                disabled
                text-color="#ff9900">
            </el-rate>
            <div class="context-des pt-3">
              <h5>{{ txt.useFriend }}</h5>
              <p>{{txt.bring}}</p>
            </div>
            <div class="card-tester">
              <div class="user-view">
                <img :src="images.testUser" alt="#">
                <div class="info-user ml-3">
                  <h6 style="color: #242f51; font-weight: bold">Zoltan Nemeth</h6>
                  <h6 style="color: #616368">CEO of Pixler Lab</h6>
                </div>
              </div>
              <div class="button-view">
                <font-awesome-icon class="mr-2" size="3x" icon="arrow-circle-left" />
                <font-awesome-icon class="ml-2" size="3x" icon="arrow-circle-right" />
              </div>
            </div>
          </div>
        </el-col>
      </el-row>
    </el-container>
  </div>
</template>

<script>
import {Images} from "@/assets/Images";

export default {
  name: "Testimonial",
  data() {
    return {
      images: {
        testier: Images.testier,
        testUser: Images.testUser
      },
      txt: {
        titleTest: 'Meet Client Satisfaction by using product',
        subTest: "The rise of mobile devices transforms the way we consume. elevant channels such as Facebook.",
        useFriend: 'User friendly & Customizable',
        bring: "Bring to the table win-win survival strategies to ensure proactive domination. At the end of the day, going forward, a new normal that has evolved from generation X is on the runway heading towards a streamlined cloud solution. User generated content in real-time will have multiple touchpoints for offshoring."
      },
      valueRate: 5
    }
  }
}
</script>

<style scoped>
.testimonial-wrapper {
  background-image: url("../../../../assets/images/map2_03.png");
  background-repeat: no-repeat;
  background-position: left top;
  background-size: initial;
  padding: 10% 0;
}

.right-test {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  text-align: left;
  margin-right: 10%;
  margin-left: 5%;
}

.card-tester {
  display: flex;
  flex-direction: row;
  width: 100%;
  align-items: center;
  justify-content: space-between;
  margin-top: 5%;
  flex-wrap: wrap;
}

p {
  color: #616368;
}

h3, h5 {
  color: #242f51;
  font-weight: bold;
}

.user-view {
  display: flex;
  align-items: center;
}
</style>
