<template>
  <div class="main">
    <div class="main__top">
      <swiper class="swiper" :options="swiperOption">
        <swiper-slide>
          <img class="aa" src="https://static11.samsungcard.com/wcms/personal/main/shpp42_35/shph42_3/__icsFiles/afieldfile/2022/12/28/p_img_1616x924.png" alt="">
          <div class="content">
            <h2>
              스타벅스 50%에 <br/>
              스트리밍 30% 할인
            </h2>
            <p class="sub">연 최대 36만원 할인,<br>모니모카드와 함께~</p>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img class="aa" src="https://static11.samsungcard.com/wcms/personal/main/shpp42_35/shph42_3/__icsFiles/afieldfile/2023/01/05/p_img_1616x924.png" alt="">
          <div class="content">
            <h2>
              연 최대 48만원 할인 <br/>
              연회비 없는 행복한 카드
            </h2>
            <p class="sub">쿠팡, 이마트 7% 할인 등<br>연 최대 48만원 할인 누려요.</p>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img class="aa" src="https://static11.samsungcard.com/wcms/personal/main/shpp42_35/shph42_3/__icsFiles/afieldfile/2022/09/29/p_img_1616x924.png" alt="">
          <div class="content">
            <h2>
              펫가족이라면 <br/>
              삼성 iD PET 카드
            </h2>
            <p class="sub">동물병원 30% 할인 등<br>연 96만원까지 할인</p>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img class="aa" src="https://static11.samsungcard.com/wcms/personal/main/shpp42_35/shph42_3/__icsFiles/afieldfile/2022/12/23/p_img_1616x924_3.png" alt="">
          <div class="content">
            <h2>
              연회비가 <br/>
              다시 내 품에~
            </h2>
            <p class="sub">모니코 가입하고<br/>카드 한 번만 쓰면 캐시백~</p>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img class="aa" src="https://static11.samsungcard.com/wcms/personal/main/shpp42_35/shph42_3/__icsFiles/afieldfile/2022/11/09/p_img_1616x924_02.png" alt="">
          <div class="content">
            <h2>
              친구에게 <br/>
              카드추천
            </h2>
            <p class="sub">카드 추천할 때마다<br/>5만원 캐시백!</p>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img class="aa" src="https://static11.samsungcard.com/wcms/personal/main/shpp42_35/shph42_3/__icsFiles/afieldfile/2022/10/13/p_img_1616x924.png" alt="">
          <div class="content">
            <h2>
              연 최대 할인금액 <br/>
              연회비의 36배?
            </h2>
            <p class="sub">교통/통신/영화/쇼핑까지 다~<br/>삼성카드 taptap O로 할인!</p>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img class="aa" src="https://static11.samsungcard.com/wcms/personal/main/shpp42_35/shph42_3/__icsFiles/afieldfile/2022/10/13/p_img_1616x924_1.png" alt="">
          <div class="content">
            <h2>
              반가운 혜택 ON! <br/>
              삼성 iD ON 카드
            </h2>
            <p class="sub">온라인 간편결제∙해외<br/>최대 1만원 할인 받아요</p>
          </div>
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
      <div class="main__login">
        <ul class="tab">
          <li @click="currentTab = i" v-for="(tab,i) in tabs" :class="{'tab__list--active':currentTab===i}" class="tab__list" :key="i">
              <div class="dd">
                {{tab}}
              </div>
          </li>
        </ul>
        <div class="tab__content">
          <div v-show="currentTab == 0" class="view">
            <div class="view__input">
              <img src="https://static12.samsungcard.com/images/personal/main/new_2204_my_login_img001.png" alt="">
              <p>삼성카드 앱의<br>
                결제 비밀번호로 로그인 해주세요.
              </p>
            </div>
            <button>
              로그인
            </button>
            <div class="view__sub">
              <a href="#">
                삼성카드 앱 안내
              </a>
              <a href="#">
                회원가입
              </a>
            </div>
          </div>
          <div v-show="currentTab == 1" class="view">
            <div class="view__input">
              <input type="text" class="input-id" placeholder="아이디 6~12자리 입력" data-format="txt" maxlength="12" title="아이디">
              <div class="id-chk">
                <div class="id-chk__button"></div>
                <label class="id-chk__save">저장</label>
              </div>
              <input type="text" class="input-pw" placeholder="비밀번호 6~20자리 입력" data-format="txt" maxlength="12" title="비밀번호">
              <div class="pw-chk">
                <div class="pw-chk__button"></div>
              </div>
            </div>
            <button>
              로그인
            </button>
            <div class="view__sub">
              <a href="#">
                아이디/비밀번호찾기
              </a>
              <a href="#">
                회원가입
              </a>
            </div>
          </div>
          <div v-show="currentTab == 2" class="view">
            <div class="view__input">
              <img src="https://static12.samsungcard.com/images/personal/main/new_2204_my_login_img002.png" alt="">
              <p>금융인증서로 로그인 해주세요.</p>
            </div>
            <button>
              로그인
            </button>
            <div class="view__sub">
              <a href="#">
                인증서등록
              </a>
              <a href="#">
                회원가입
              </a>
            </div>
          </div>
          <div v-show="currentTab == 3" class="view">
            <div class="view__input">
              <img src="https://static12.samsungcard.com/images/personal/main/new_2204_my_login_img003.png" alt="">
              <p>공동인증서로 로그인 해주세요.</p>
            </div>
            <button>
              로그인
            </button>
            <div class="view__sub">
              <a href="#">
                인증서등록
              </a>
              <a href="#">
                회원가입
              </a>
            </div>
          </div>
        </div>
        <ul class="other">
          <li>
            <a href="#">
              <img src="//static11.samsungcard.com/wcms/personal//images/main/new_2204_my_login_ico001.png" alt="">
              <p>명세서</p>
            </a>
          </li>
          <li>
            <a href="#">
              <img src="//static11.samsungcard.com/wcms/personal//images/main/new_2204_my_login_ico002.png" alt="">
              <p>이용내역</p>
            </a>
          </li>
          <li>
            <a href="#">
              <img src="//static11.samsungcard.com/wcms/personal//images/main/new_2204_my_login_ico004.png" alt="">
              <p>즉시결제</p>
            </a>
          </li>
          <li>
            <a href="#">
              <img src="//static11.samsungcard.com/wcms/personal//images/main/new_2204_my_login_ico003.png" alt="">
              <p>분할납부</p>
            </a>
          </li>

        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

export default {
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
      tabs: ['앱카드','아이디','금융인증서','공동인증서'],
    }
  }
}
</script>

<style lang="scss" scoped>

.main {
  margin-top: 50px;
  &__top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 1224px;
    margin: 0 auto 41px auto;
  }
  &__login {
    flex: 0 0 392px;
    height: 462px;
    border: 1px solid #e2e5eb;
    padding: 24px 17px;
    border-radius: 16px;
    box-sizing: border-box;
    position: relative;

    .tab {
      display: flex;
      justify-content: center;
      border-bottom: 1px solid #e2e5eb;

      &__list {
        width: 25%;
        text-align: center;
        font-size: 14px;
        color: #666666;
        padding: 16px 0;
        cursor: pointer;

        &--active {
          font-weight: bold;
          color: #111111;
          border-bottom: 2px solid black;
        }
      }
      &__content {
        .view {
          width: 100%;
          margin: 0 auto;
          padding: 0 15px;
          box-sizing: border-box;
          position: relative;
          &__input {
            padding-top: 30px;
            text-align: center;
            height: 168px;
            box-sizing: border-box;

            .input-id {
              width: 100%;
              height: 52px;
              border-radius: 10px;
              box-sizing: border-box;
              border: 1px solid #dcdcdc;
              padding-left: 20px;
              padding-bottom: 0px;
              position: relative;
            }
            .input-pw {
              width: 100%;
              height: 52px;
              border-radius: 10px;
              box-sizing: border-box;
              border: 1px solid #dcdcdc;
              padding-left: 20px;
              padding-bottom: 0px;
              position: relative;
              background-color: rgb(236, 235, 230);
              margin-top: 16px;
            }
            .id-chk {
              position: absolute;
              right: 8%;
              top: 20%;
              margin-top: -11.5px;
              display: flex;

              &__button {
                display: inline-block;
                width: 23px;
                height: 23px;
                background: url("https://static12.samsungcard.com/images/personal/common/bg_form_blue_small.png") no-repeat -50px 0;
                vertical-align: middle;
              }
              &__save {
                font-size: 14px;
                color: #888888;
                margin-left: 5px;
              }
            }
            .pw-chk {
              position: absolute;
              right: 8%;
              top: 44%;
              margin-top: -11.5px;
              display: flex;
              &__button {
                width: 20px;
                height: 20px;
                background: url("https://static12.samsungcard.com/images/personal/main/new_2204_my_login_mouse.png");
                background-size: 20px 20px;
                right: 16px;
                top: 50%;
              }
            }
          }
          &__sub {
            display: flex;
            justify-content: space-between;
            margin-top: 24px;
            padding-bottom: 24px;
            border-bottom: 1px solid #e2e5eb;
            font-size: 14px;
            color: #666666;
          }
          img {
            margin-bottom: 12px;
            width: 48px;
            height: 48px;
          }
          p {
            font-size: 16px;
            line-height: 24px;
            font-weight: bold;
          }
          button {
            width: 100%;
            height: 52px;
            line-height: 52px;
            background: #2090ff;
            border-radius: 10px;
            color: #ffffff;
            text-align: center;
          }
        }
      }
    }
    .other {
      display: flex;
      justify-content: space-around;
      width: 100%;
      padding-top: 19px;
      box-sizing: border-box;

      li {
        color: #111111;
        text-align: center;
      }
      img {
        width: 24px;
        height: 24px;
        margin-bottom: 8px;
      }
      p {
        line-height: 18px;
      }
    }
  }
}

.swiper {
  background: none;
  width: 808px;
  height: 462px;
  margin: 0;
  .swiper-slide {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;

    .content {
      position: absolute;
      top: 60px;
      left: 52px;
      color: #ffffff;

      h2 {
        font-size: 36px;
        font-weight: bold;
        line-height: 1.33;
      }
      .sub {
        font-size: 16px;
        font-weight: bold;
        line-height: 1.33;
        margin-top: 10px;
      }
    }
  }
}

.aa {
  width: auto;
  height: 462px;
  border-radius: 10px;
}

.swiper-container-horizontal > .swiper-pagination-bullets {
  bottom: 60px;
  left: 52px;
  font-size: 16px;
  display: flex;
  align-items: center;
  width: 100%;
}

.swiper-pagination {
  position: absolute;
  text-align: center;
  transition: 300ms opacity;
  transform: translate3d(0, 0, 0);
  z-index: 10;
}
</style>
