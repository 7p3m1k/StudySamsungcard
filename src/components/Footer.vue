<template>
  <div>
    <footer>
      <div class="footer-wrap">
        <div class="phone-number">
          <ul>
            <li><strong>ARS (유로)</strong></li>
            <li>대표전화
              <a href="#">1588-8700</a>
            </li>
            <li>카드신청
              <a href="#">1688-1133</a>
            </li>
            <li>분실신고·한도승인 (국내)
              <a href="#">1588-8900</a>
            </li>
            <li>(해외)
              <a href="#">82-2-2000-8100, 800-1588-8700</a>
            </li>
          </ul>
        </div>
        <div class="info">
          <div class="info-top">
            <ul>
              <li><strong>회사소개</strong></li>
              <li>ENGLISH</li>
              <li>전자민원접수</li>
              <li>이용약관</li>
              <li>고객권리 안내</li>
              <li>금융사기피해예방</li>
            </ul>
            <div class="family-site">
              <select onchange="if(this.value) window.open(this.value)">
                <option value="" disabled selected>패밀리 사이트</option>
                <option value="https://www.naver.com">쇼핑</option>
                <option value="https://www.daum.net">여행</option>
                <option value="https://www.kakaocorp.com/page/">웨딩</option>
                <option value="#">보험</option>
              </select>
            </div>
          </div>

          <div class="sub">
            <ul>
              <li><strong>개인정보 처리방침</strong></li>
              <li><strong>위치기반서비스 이용약관</strong></li>
              <li>통신중개판매상품 이메일 <span>lifecare.scard@samsung.com</span></li>
            </ul>
            <div class="sub__right">사업자정보 확인 ></div>
          </div>
        </div>
        <div class="info2">
          <ul>
            <li>대표이사 사장 김대환</li>
            <li>서울 중구 세종대로 67 (04514)</li>
            <li>사업자등록번호 202-81-45602</li>
            <li>통신판매업 신고번호 제 2009-서울중구-1449호</li>
          </ul>
        </div>
        <div class="copyright">
          <p>© SAMSUNG CARD CO., LTD. All rights reserved.</p>
          <img src="https://static11.samsungcard.com/wcms/footer/images/common/new_2204_p_f_logo.png" alt="">
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import {Swiper, SwiperSlide} from "vue-awesome-swiper";

export default {
  name: "Footer.vue",

  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      swiperOption: {
        slidesPerView: 4,
        spaceBetween: 10,
        slidesPerGroup: 4,
        loop: true,
        loopFillGroupWithBlank: true,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      },
    }
  }
}
</script>

<style lang="scss" scoped>

footer {
  background-color: #F3F5F8;
  padding: 37px 0 38px;

  .footer-wrap {
    max-width: 944px;
    min-width: 1136px;
    margin: 0 auto;
  }
  .phone-number {
    ul {
      display: flex;
      border-bottom: 1px solid #e0e0e0;
      padding-bottom: 12px;

      li {
        strong {
          border-right: 1px solid #888;
          padding-right: 8px;
        }
      }
      li:nth-child(2){
        padding-left: 8px;
      }
    }
  }

  .info-top {
    display: flex;
    justify-content: space-between;
  }

  .info {
    ul {
      display: flex;

      li {
        padding: 7px 0 0 9px;
        font-size: 14px;
        background-position: 0 11px;
      }
      li::after {
        content: '';
        padding-right: 8px;
        border-right: 1px solid #888888;
      }
      li:last-child::after {
        content: none;
      }
      li:first-child {
        padding: 7px 0 0 0;
      }
    }
    .family-site {
      select {
        margin-top: 7px;
        width: 182px;
        height: 30px !important;
        border: 1px solid #808789 !important;
        font-size: 16px;
        color: #7b7e86;
        padding: 0 11px;
      }
      select option[value=""][disabled] {
        display: none;
      }
    }
  }
  .sub {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 70%;
    ul {
      //display: flex;
    }
    &__right {
      padding-top: 7px;
    }
    &__right:hover {
      text-decoration: underline;
      cursor: pointer;
    }
  }
  .info2 {
    padding-top: 17px;
    font-size: 14px;
    ul {
      display: flex;
      li {
        margin-right: 20px;
        letter-spacing: -1px;
      }
    }
  }
  .copyright {
    padding-top: 14px;
    color: #7b7e86;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}


</style>