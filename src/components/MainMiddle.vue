<template>
  <div class="main-middle">
    <ul class="tab">
      <li @click="currentTab = i" v-for="(tab,i) in tabs" :class="{'tab__list--active':currentTab===i}" class="tab__list" :key="i">
        <div class="dd">
          <span>{{tab}}</span>
          <p class="ddb" :class="{'ddb--active':currentTab ===i}">카드</p>
        </div>
      </li>
    </ul>
    <div class="right-button">
      <a>
        <span>내게 맞는 카드 찾기</span>
      </a>
      <a>
        <span>친구에게 카드 추천</span>
      </a>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

export default {
  name: "MainMiddle.vue",
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        }
      },
      currentTab: 0,
      tabs: ['개인','법인'],
    }
  }
}
</script>

<style lang="scss" scoped>
.main-middle {
  border: 1px solid #e2e5eb;
  border-radius: 12px;
  padding: 32px 24px;
  max-width: 1224px;
  margin: 0 auto;
  box-sizing: border-box;
  position: relative;
  display: flex;
  justify-content: space-between;
}

.tab {
  display: flex;

  &__list {
    font-size: 14px;
    color: #666666;
    cursor: pointer;

    .dd {
      display: inline-block;
      text-align : center;
      vertical-align: top;
      font-size: 16px;
      font-weight: bold;
      line-height: 18px;

      .ddb {
        display: none;
        &--active {
          display: inline-block;
        }
      }
    }

    &--active {
      color: #111111;
    }

    &--active::after {
      content: '';
      display: inline-block;
      margin-left: 4px;
      width: 15px;
      height: 15px;
      background-size: cover;
      background-image: url("https://static12.samsungcard.com/images/personal/common/new_2203_r_arrow.png");
    }
  }
  &__list:last-child::before {
    content: '';
    display: inline-block;
    width: 1px;
    height: 16px;
    margin: 0 12px 0 5px;
    vertical-align: top;
    background: #e2e5eb;
  }
}

.right-button {
  display: flex;

  a {
    margin: 0 4px;
    padding: 3px 19px;
    border-radius: 16px;
    background: #f4f6fb;

    span {
      line-height: 28px;
      font-size: 14px;
      color: #111111;
    }
  }
}
</style>