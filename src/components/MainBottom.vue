<template>
    <div class="main-bottom">
      <div class="main-bottom-wrapper">
        <div class="item bg">
          <div class="item__left">
            <div class="item__head">금융 ></div>
            <p class="item__title">
              목돈이 필요할때 상환수수료 없이! <br/>
              장기카드대출!
            </p>
            <p class="item__sub">
              최대 5,000만원, 최저이율 4.9%
            </p>
          </div>
          <div>
            <img src="https://static11.samsungcard.com/wcms/personal//images/main/new_2204_my_mid001.png" alt="">
          </div>
        </div>
        <div class="item">
          <div class="item__text">
            <div>쇼핑 ></div>
            <p class="item__title">
              10시 일일특가 <br/>
            </p>
            <p class="item__desc">
              [6일2시][2천원쿠폰]마름모 실크 스카프 2WSD366 5종 택1
              </p>
            <p class="item__sub">
              무료배송 <span>600개 한정</span>
            </p>
            <p class="item__price">26,900원</p>
          </div>
          <div>
            <img src="https://static21.samsungcard.com/imageq/LK_250x250/Q_90/date/2023020615/src/goods/23/01/S23010084090009.jpg" alt="">
          </div>
        </div>
      </div>
      <div class="main-bottom__event">
        <div class="event__left">
          <ul>
            <li>
              <a href="#">
                <div class="img-wrap">
                  <img src="https://static11.samsungcard.com/wcms/event/general_v2/__icsFiles/afieldfile/2023/02/01/P_thumb_286x275_6.png" alt="">
                </div>
                <div class="event-card">
                  <p class="name">카드 할부로 새 차 사면 최대 10만 포인트 선물</p>
                  <p class="date">2023.02.03~2023.02.28</p>
                </div>
              </a>
            </li>
            <li>
              <a href="#">
                <div class="img-wrap">
                  <img src="https://static11.samsungcard.com/wcms/event/general_v2/__icsFiles/afieldfile/2022/11/18/P_thumb_286x275.png" alt="">
                </div>
                <div class="event-card">
                  <p class="name">리틀프렌즈 백팩 선물 <br/>
                    국민행복 삼성카드 V2
                  </p>
                  <p class="date">2023.02.03~2023.02.28</p>
                </div>
              </a>
            </li>
            <li>
              <a href="#">
                <div class="img-wrap">
                  <img src="https://static11.samsungcard.com/wcms/event/general_v2/__icsFiles/afieldfile/2022/12/21/P_thumb_286x275_12.png" alt="">
                </div>
                <div class="event-card">
                  <p class="name">다이렉트로 부담없이 캐시백 혜택까지</p>
                  <p class="date">2023.02.03~2023.02.28</p>
                </div>
              </a>
            </li>
          </ul>
          <button class="more-btn" type="button">
            <div>진행중 이벤트 더보기</div>
          </button>
        </div>
        <div class="event__right">
          <ul>
            <li>
              <span class="badge">게임존</span>
              <div class="text-box">
                <p class="title">게임도하고<br/>혜택도 받고!</p>
                <p class="sub">매일매일 다양한 혜택받기</p>
              </div>
              <div class="img-wrapper">
                <img src="https://static11.samsungcard.com/wcms/personal/main/shph42_4/__icsFiles/afieldfile/2022/06/07/new_2204_my_r_img001.png" alt="">
              </div>
            </li>
            <li>
              <span class="badge">정기결제</span>
              <div class="text-box">
                <p class="title">잊기 쉬운<br/>생활요금 납부</p>
                <p class="sub">자동납부로 편리하게 <br/> 이용하세요.</p>
              </div>
              <div class="img-wrapper">
                <img src="https://static11.samsungcard.com/wcms/personal/main/shph42_4/__icsFiles/afieldfile/2022/06/07/new_2204_my_r_img002.png" alt="">
              </div>
            </li>
            <li>
              <span class="badge">자동차</span>
              <div class="text-box">
                <p class="title">차 살 때<br/>더 좋은 혜택</p>
                <p class="sub">신차/중고차 구매 계획이 <br/> 있으시다면</p>
              </div>
              <div class="img-wrapper">
                <img src="https://static11.samsungcard.com/wcms/personal/main/shph42_4/__icsFiles/afieldfile/2022/06/07/new_2204_my_r_img004.png" alt="">
              </div>
            </li>
            <li>
              <span class="badge">보험</span>
              <div class="text-box">
                <p class="title">이제 필요한 보험은 <br/>다이렉트로</p>
                <p class="sub">간편한 다이렉트 가입</p>
              </div>
              <div class="img-wrapper">
                <img src="https://static11.samsungcard.com/wcms/personal/main/shph42_4/__icsFiles/afieldfile/2022/06/07/new_2204_my_r_img005.png" alt="">
              </div>
            </li>
          </ul>
         </div>
      </div>
    </div>
</template>

<script>
export default {
  name: "MainBottom.vue"
}
</script>

<style lang="scss" scoped>
.main-bottom {
  max-width: 1224px;
  margin: 24px auto 60px;

  .item {
    display: flex;
    justify-content: space-between;
    width: 50%;
    border-radius: 12px;
    padding: 32px 24px;
    box-sizing: border-box;
    line-height: 18px;
    border: 1px solid #e2e5eb;
    margin-bottom: 24px;

    &__text {
      max-width: 320px
    }
    &__desc {
      margin: 16px 0 8px;
      color: #111;
    }

    &__title {
      font-size: 23px;
      line-height: 26px;
      color: #111111;
      font-weight: bold;
      margin-top: 16px;
    }
    img {
      width: 188px;
      height: 210px
    }
    &__sub {
      display: flex;
      align-items: center;
      font-size: 14px;
      color: #666666;
      margin-top: 8px;
    }
    &__sub>span::before {
      content: "";
      margin-right: 4px;
      border: 1px solid #e2e5eb;
    }
    &__price {
      margin-top: 45px;
      font-size: 24px;
      font-weight: bold;
      color: #111111;
    }

    &__head {
      font-size: 16px;
      color: #111111;
      font-weight: bold;
      display: flex;
      align-items: center;
      line-height: 18px;
    }
  }

  .bg {
    background-color: #dcf2fe;
    border: none;
  }

  .main-bottom-wrapper {
    display: flex;
    gap: 2%;
  }

  &__event {
    display: flex;
    justify-content: space-between;

    .event {
      &__left {
        ul {
          display: flex;
          justify-content: space-between;
          margin-bottom: 24px;
          gap: 20px;
          li {
            border-radius: 12px;
            background: #f3f6fb;
            width: 255px;

            a {
              .img-wrap {
                overflow: hidden;
                border-radius: 12px 12px 0 0;
                img {
                  width: 100%;
                  height: auto;
                }
              }
              .event-card {
                font-weight: bold;
                line-height: 20px;
                padding: 24px 0 36px 0;
                box-sizing: border-box;
                text-align: center;
                .name {
                  color: #111111;
                  padding: 0 30px;
                }
                .date {
                  font-size: 14px;
                  line-height: 20px;
                  color: #666666;
                  margin-top: 8px;
                  padding: 0 30px;
                }
              }
            }
          }
        }
        .more-btn {
          width: 100%;
          display: flex;
          justify-content: center;
          div {
            width: 100%;
            background: #f4f6fb;
            border: 1px solid #f4f6fb;
            font-size: 14px;
            line-height: 14px;
            padding: 13px 14px 12px;
            border-radius: 12px;
            font-weight: bold;
          }
        }
      }
      &__right {
        ul {
          min-width: 400px;
          li {
            height: 140px;
            background: #f9fafc;
            border-radius: 12px;
            margin-bottom: 24px;
            padding: 32px 0 32px 24px;
            position: relative;

            .badge {
              padding: 4px 8px 3px;
              border-radius: 28px;
              color: #fff;
              text-align: center;
              font-size: 12px;
              line-height: 12px;
              background-color: #111111;
            }
            .text-box {
              .title {
                font-size: 24px;
                line-height: 26px;
                color: #111111;
                font-weight: bold;
                margin-top: 16px;
              }
              .sub {
                font-size: 16px;
                line-height: 18px;
                color: #666666;
                margin-top: 8px;
              }
            }
            .img-wrapper {
              position: absolute;
              top: 0;
              right: 0;

              img {
                width: 150px;
                height: 200px;
              }
            }
          }
        }
      }
    }
  }
}

</style>