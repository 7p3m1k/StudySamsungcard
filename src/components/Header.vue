<template>
  <header class="header">
    <div class="sub">
      <ul class="sub__left">
        <li class="">
          <a href="">개인사업자</a>
        </li>
        <li>
          <a href="">법인</a>
        </li>
        <li>
          <a href="">가맹점</a>
        </li>
        <li>
          <a href="">금융소비자보호</a>
        </li>
        <li>
          <a href="">상품공시실</a>
        </li>
      </ul>
      <ul class="sub__right">
        <li>로그인</li>
        <li>회원가입</li>
      </ul>
    </div>
    <div class="nav">
      <div class="nav__logo">
        <a href="#"></a>
      </div>
      <ul class="nav__menu">
        <li class="nav__list"><a href="">마이</a></li>
        <li class="nav__list"><a href="">혜택</a></li>
        <li class="nav__list"><a href="">카드안내/신청</a></li>
        <li class="nav__list"><a href="">금융</a></li>
        <li class="nav__list"><a href="">정기결제</a></li>
        {{scrollChecked}}
      </ul>
      <div class="nav__sub">
        <button class="search"> </button>
        <button class="hamburger"></button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header.vue",
  data(){
    return {
      scrollChecked: false,
    }
  },
  mounted () {
    // let context = this
    window.addEventListener('scroll', this.aa)
  },
  beforeDestroy () {
    window.removeEventListener('keyup', this.aa)
  },
  methods: {
    aa(){
      if(window.scrollY > 0) {
        console.log('내려갈때',this.scrollChecked = true)
      }
      if(window.scrollY === 0){
        console.log('제자리일때',this.scrollChecked = false)
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  max-width: 1224px;
  margin: 0 auto;

  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background-color: #ffffff;
  z-index: 99999;

  .sub {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 28px 0px 36px;
    box-sizing: border-box;
    &__left {
      display: flex;

      li {
        display: inline-flex;
        align-items: center;
        position: relative;
        height: 24px;
        font-size: 14px;
        line-height: 24px;
        font-weight: bold;

        a {
          color: #666;
        }
      }

      li::after {
        content: "";
        display: inline-block;
        background-color: #e2e5eb;
        width: 1px;
        height: 12px;
        margin: 0 10px;
      }
      li:last-child::after {
        content: none;
      }
    }
    &__right {
      display: flex;

      li::after {
        content: "";
        display: inline-block;
        background-color: #e2e5eb;
        width: 1px;
        height: 12px;
        margin: 0 10px;
      }
      li:last-child::after {
        content: none;
      }
    }
  }

  .nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 0px 50px;
    background-color: #fff;

    &__logo{
      a {
        display: inline-block;
        width: 158px;
        height: 22px;
        padding: 0px;
        background: url("https://static12.samsungcard.com/images/personal/common/new_2204_p_h_logo.png");
        background-size: 158px 22px;
      }
    }
    &__menu {
      display: flex;
    }
    &__list {
      a {
        display: block;
        position: relative;
        margin-left: 73px;
        font-size: 20px;
        line-height: 22px;
        font-weight: bold;
        white-space: nowrap;
        color: #111;
      }
    }
    &__sub {
      display: flex;
      .search {
        width: 20px;
        height: 20px;
        padding: 0px;
        background: url("https://static12.samsungcard.com/images/personal/common/new_2204_search.png");
        background-size: 20px 20px;
        margin-right: 16px;
      }
      .hamburger {
        margin-top: 0px;
        width: 20px;
        height: 20px;
        padding: 0px;
        background: url("https://static12.samsungcard.com/images/personal/common/new_2204_h_menu.png");
        background-size: 20px 20px;
      }
    }
  }
}


</style>