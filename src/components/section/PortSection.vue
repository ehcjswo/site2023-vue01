<template>
  <section id="portSection" :class="attr">
    <h3>대표 메뉴 구경하기</h3>
    <p>세계적으로 유명하고 대표적인 음식 종류</p>
    <div class="port__inner container">
      <div class="port__btn"></div>
      <div class="port__cont">
        <!-- <div class="port">
           <figure class="port__header">
            <router-link to="/"
              ><img src="@/assets/images/port/port01.png" alt="포트폴리오"
            /></router-link>
          </figure>
          
          <div class="port__body">
            <span>
              <img src="@/assets/images/member/member80.svg" alt="김땡땡" />
            </span>
            <div>
              <h4>진현미 포트폴리오</h4>
              <p>프론트앤드 개발자 포트폴리오</p>
            </div>
          </div> 
        </div> -->

        <div class="port" v-for="(text, index) in texts" :key="index">
          <figure class="port__header">
            <router-link to="/">
              <img :src="text.img" :alt="text.title" />
            </router-link>
          </figure>

          <div class="port__body">
            <span>
              <img :src="text.icon" alt="이름" />
            </span>
            <div>
              <h4>{{ text.title }}</h4>
              <p>{{ text.desc }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
  },
  data: function () {
    return {
      texts: [
        {
          img: "./images/port/koreafood_1.png",
          title: "김소희",
          desc: "대한민국 셰프",
          icon: "./images/port/profileM_1.png",
        },
        {
          img: "./images/port/koreafood_2.png",
          title: "차민욱",
          desc: "대한민국 셰프",
          icon: "./images/port/profileM_2.png",
        },
        {
          img: "./images/port/koreafood_3.png",
          title: "최현석",
          desc: "대한민국 셰프",
          icon: "./images/port/profileM_3.png",
        },
        {
          img: "./images/port/koreafood_4.png",
          title: "천설희 포트폴리오",
          desc: "대한민국 셰프",
          icon: "./images/port/profileM_4.png",
        },
        {
          img: "./images/port/koreafood_5.png",
          title: "이원일",
          desc: "대한민국 셰프",
          icon: "./images/port/profileM_5.png",
        },
        {
          img: "./images/port/koreafood_6.png",
          title: "김풍",
          desc: "대한민국 셰프",
          icon: "./images/port/profileM_6.png",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
// ports__wrap
.ports__wrap {
  > p {
    margin-top: 10px;
  }
  .port__inner {
    .port__cont {
      @include flex-center;
      flex-wrap: wrap;

      .port {
        width: 32%;
        .port__header {
          img {
            height: 272px;
            border-radius: 10px;
          }
        }
        .port__body {
          display: flex;
          margin-top: 15px;
          margin-bottom: 30px;
          position: relative;

          > span {
            img {
              border-radius: 50%;
              width: 50px;
              height: 50px;
            }
          }
          &::before {
            content: "";
            width: 50px;
            height: 50px;
            background-color: #0f035d;
            position: absolute;
            border-radius: 50%;
            top: 0;
            left: 0;
            z-index: -999;
          }
          > div {
            text-align: left;
            margin-left: 10px;
            h4 {
              font-size: 20px;
              font-weight: 400;
            }
            p {
              font-size: 16px;
              color: #2c3a4b;
              font-weight: 300;
            }
          }
        }
        &:nth-child(1) .port__body::before {
          background-color: #fa635c;
        }
        &:nth-child(2) .port__body::before {
          background-color: #fee580;
        }
        &:nth-child(3) .port__body::before {
          background-color: #d6d4ed;
        }
        &:nth-child(4) .port__body::before {
          background-color: #f4d6ba;
        }
        &:nth-child(5) .port__body::before {
          background-color: #b2b764;
        }
        &:nth-child(6) .port__body::before {
          background-color: #837673;
        }
      }
    }
  }
}
</style>
