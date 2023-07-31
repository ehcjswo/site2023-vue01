<template>
  <footer id="footer" class="footer__wrap section Nanum5" role="contentinfo">
    <div class="footer__inner container">
      <div class="footer__text">
        <h5>KDH</h5>
        <p>
          안녕하세요! <br />
          더 다양한 정보와 문의는 이메일을 통해주세요 <br />
          ehcjswo1@gmail.com
        </p>
        <ul class="sns">
          <li>
            <router-link to="/">
              <!-- <img src="@/assets/images/footer/snsIcon.svg" alt="페이스북" /> -->
            </router-link>
          </li>
          <li>
            <router-link to="/">
              <!-- <img src="@/assets/images/footer/snsIcon.svg" alt="인스타그램" /> -->
            </router-link>
          </li>
          <li>
            <router-link to="/">
              <!-- <img src="@/assets/images/footer/snsIcon.svg" alt="유튜브" /> -->
            </router-link>
          </li>
          <li>
            <router-link to="/">
              <!-- <img src="@/assets/images/footer/snsIcon.svg" alt="깃헙" /> -->
            </router-link>
          </li>
        </ul>
      </div>
      <div class="footer__menu">
        <div>
          <h4>사이트</h4>
          <ul>
            <li>
              <router-link to="/">웹표준 사이트</router-link>
            </li>
            <li>
              <router-link to="/">반응형 사이트</router-link>
            </li>
            <li>
              <router-link to="/">패럴랙스 사이트</router-link>
            </li>
            <li>
              <router-link to="/">포트폴리오 사이트</router-link>
            </li>
          </ul>
        </div>
        <div>
          <h4>유형</h4>
          <ul>
            <li>
              <router-link to="/">이미지 유형</router-link>
            </li>
            <li>
              <router-link to="/">카드 유형</router-link>
            </li>
            <li>
              <router-link to="/">이미지/텍스트 유형</router-link>
            </li>
            <li>
              <router-link to="/">배너 유형</router-link>
            </li>
            <li>
              <router-link to="/">텍스트 유형</router-link>
            </li>
            <li>
              <router-link to="/">푸터 유형 </router-link>
            </li>
          </ul>
        </div>
        <div>
          <h4>스크립트</h4>
          <ul>
            <li>
              <router-link to="/">검색 이펙트</router-link>
            </li>
            <li>
              <router-link to="/">퀴즈 이펙트</router-link>
            </li>
            <li>
              <router-link to="/">마우스 이펙트</router-link>
            </li>
            <li>
              <router-link to="/">슬라이드 이펙트</router-link>
            </li>
            <li>
              <router-link to="/">패랠랙스 이펙트</router-link>
            </li>
            <li>
              <router-link to="/">게임 이팩트</router-link>
            </li>
          </ul>
        </div>
        <div>
          <h4>레퍼런스</h4>
          <ul>
            <li>
              <router-link to="/">CSS</router-link>
            </li>
            <li>
              <router-link to="/">FONTS</router-link>
            </li>
            <li>
              <router-link to="/">BLOG</router-link>
            </li>
            <li>
              <router-link to="/">REFERENCE</router-link>
            </li>
            <li>
              <router-link to="/">TUTORIAL</router-link>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer__right">
        <p>Copyright 2022. All Rights Reserved. - Designed by KDH</p>
      </div>
    </div>
  </footer>
</template>
<style lang="scss">
//footer__wrap
.footer__wrap {
  .footer__inner {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    .footer__text {
      width: 30%;
      > h5 {
        font-size: 18px;
        line-height: 1.2;
        font-weight: 400;
        margin-bottom: 25px;
      }
      > p {
        font-size: 14px;
        line-height: 1.7;
        font-weight: 400;
        color: #909090;
        margin-bottom: 30px;
      }
      > ul {
        > li {
          display: inline;
          > a {
            display: inline-block;
            width: 45px;
            height: 45px;
            background-color: #fff;
            background-image: url(../../assets/images/footer/snsIcon.svg);
            border-radius: 50%;
            transition: background-color 0.3s;
          }
          a:hover {
            background-color: #e0e9ff;
          }
          &:nth-child(2) a {
            background-position: -45px 0;
          }
          &:nth-child(3) a {
            background-position: -90px 0;
          }
          &:nth-child(4) a {
            background-position: -135px 0;
          }
        }
      }
    }
    .footer__menu {
      width: 70%;
      display: flex;
      > div {
        width: 25%;
        > h4 {
          font-size: 18px;
          font-weight: 400;
          margin-bottom: 20px;
        }
        > ul {
          > li {
            > a {
              font-weight: 400;
              color: #808080;
              font-size: 14px;
            }
          }
        }
      }
    }
    .footer__right {
      width: 100%;
      padding: 30px;
      text-align: center;
      border-top: 1px solid #e5e5e5;
      margin-top: 50px;
      color: #808080;
      font-size: 14px;
    }
  }
}
</style>
