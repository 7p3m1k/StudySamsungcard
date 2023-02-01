<template>
  <div class="main-middle">
    <div class="tab-wrapper">
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

    <div>
      <div v-show="currentTab == 0">
        <swiper class="swiper" :options="swiperOption">
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/personal/b_AAP1742_02.png" alt="">
              <p class="card__name">모니모카드</p>
              <p class="card__desc">스타벅스 50%, <br>스트리밍 30% 할인</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/personal/b_AAP1688.png" alt="">
              <p class="card__name">국민행복 삼성카드 V2</p>
              <p class="card__desc">다양한 국가바우처 사용에 <br>일상 할인 혜택까지!</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/personal/b_AAP1773.gif" alt="">
              <p class="card__name">삼성 iD PET 카드</p>
              <p class="card__desc">펫가족을 위한 라이프 케어 카드</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/personal/b_AAP1483.png" alt="">
              <p class="card__name">삼성카드 taptap O</p>
              <p class="card__desc">친구추천 1위 카드 <br>연 최대 36만원 할인!</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/personal/DN_AAP1731.gif" alt="">
              <p class="card__name">삼성 iD ON 카드</p>
              <p class="card__desc">맛있는 <br>자동 맞춤 30% 할인</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/personal/b_AAP1742_02.png" alt="">
              <p class="card__name">모니모카드</p>
              <p class="card__desc">스타벅스 50%, <br>스트리밍 30% 할인</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/personal/b_AAP1742_02.png" alt="">
              <p class="card__name">모니모카드</p>
              <p class="card__desc">스타벅스 50%, <br>스트리밍 30% 할인</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/personal/b_AAP1742_02.png" alt="">
              <p class="card__name">모니모카드</p>
              <p class="card__desc">스타벅스 50%, <br>스트리밍 30% 할인</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/personal/b_AAP1742_02.png" alt="">
              <p class="card__name">모니모카드</p>
              <p class="card__desc">스타벅스 50%, <br>스트리밍 30% 할인</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/personal/b_AAP1742_02.png" alt="">
              <p class="card__name">모니모카드</p>
              <p class="card__desc">스타벅스 50%, <br>스트리밍 30% 할인</p>
            </div>
          </swiper-slide>
          <div class="swiper-button-prev" slot="button-prev"></div>
          <div class="swiper-button-next" slot="button-next"></div>
        </swiper>
      </div>
      <div v-show="currentTab == 1">
        <swiper class="swiper" :options="swiperOption1">
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/corporation/b_AAP1743.gif" alt="">
              <p class="card__name">CORPORATE #7 MORE</p>
              <p class="card__desc">사업에 힘이  되도록, <br>적립을 더</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/corporation/b_AAP1677.png" alt="">
              <p class="card__name">CORPORATE #2</p>
              <p class="card__desc">국내외 0.2% 캐시백</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/corporation/b_AAP1677.png" alt="">
              <p class="card__name">CORPORATE GLOBAL</p>
              <p class="card__desc">국내 0.2%, 해외 0.6% <br/> 캐시백 혜택</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/corporation/b_AAP1677.png" alt="">
              <p class="card__name">CORPORATE</p>
              <p class="card__desc">기업과 임직원을 위해<br>꼭 필요한 것에 집중</p>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <img src="https://static11.samsungcard.com/wcms/home/scard/image/corporation/b_AAP1018.png" alt="">
              <p class="card__name">삼성스카이패스법인카드</p>
              <p class="card__desc">스카이패스 마일리지 혜택</p>
            </div>
          </swiper-slide>
          <div class="swiper-button-prev" slot="button-prev"></div>
          <div class="swiper-button-next" slot="button-next"></div>
        </swiper>
      </div>
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
        slidesPerView: 5,
        spaceBetween: 60,
        slidesPerGroup: 5,
        loop: true,
        loopFillGroupWithBlank: true,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      },
      swiperOption1: {
        slidesPerView: 5,
        spaceBetween: 60,
        slidesPerGroup: 0,
        loop: true,
        loopFillGroupWithBlank: true,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
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
}

.tab-wrapper {
  display:  flex;
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
      cursor: pointer;
    }
  }
}

.card {
  text-align: center;
  width: 202px;
  img {
    width: 120px;
  }
  &__name {
    font-size: 16px;
    font-weight: bold;
    color: #111111;
    line-height: 20px;
    margin-top: 20px;
    min-height: 40px;
  }
  &__desc {
    font-size: 14px;
    color: #666666;
    line-height: 20px;
    margin-top: 5px;
  }
}

.swiper {
  margin-top: 32px;
  padding: 0 60px;
}

.swiper-button-prev {
  background: url("https://static12.samsungcard.com/images/personal/main/new_2204_my_swiper_prev.png") no-repeat 0 0;
  background-size: 32px 32px;
}

.swiper-button-next {
  background: url("https://static12.samsungcard.com/images/personal/main/new_2204_my_swiper_next.png") no-repeat 0 0;
  background-size: 32px 32px;
}

 .swiper-button-prev:after, .swiper-button-next:after {
   content: none;
 }

</style>