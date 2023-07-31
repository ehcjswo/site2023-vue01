<template>
  <section id="introSection" :class="attr">
    <h3 class="blind">프론트앤드 커리큘럼 과정 소개</h3>
    <div class="intro__inner container">
      <div class="intro__title">
        <span>Portfolio</span>
        <h3 v-html="title"></h3>
        <p v-html="desc"></p>
      </div>
      <div class="intro__desc">
        <div v-for="(text, index) in texts" :key="index">
          <h4 :class="'icon-bg' + (index + 1)">{{ text.title }}</h4>
          <p>
            {{ text.desc }}
          </p>
        </div>
        <!-- <div>
          <router-link to="https://kebab00.tistory.com/"
            ><h4 class="icon-bg1">Tistory</h4></router-link
          >
          <p>
            수업을 시작하면서 개설한 Tistory 블로그 입니다. 그동안 배운 것들을
            모두 정리하고 복습한 사이트이며 HTML, CSS, PHP, JavaScript,
            Programmers등이 정리되어 있습니다.
          </p>
        </div> -->
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
      title: " 한국<br/>유명한 셰프",
      desc: "한국에서 유명한 셰프들의 다양한 음식 <br/>여러분들도 도전해보세요!",
      texts: [
        {
          title: "한식",
          desc: " 건강하고 균형 잡힌 식단. 한식은 쌀, 김치, 채소, 고기등 다양한 식재료를 사용하여 영양 균형을 중요시 합니다.",
        },
        {
          title: "중식",
          desc: "매우 다양한 맛과 향: 중국 음식은 달콤한, 짭짤한, 매운, 쓴 맛 등 다양한 맛을 가집니다. 향신료와 조미료를 많이 사용하여 풍부한 향을 내며, 지역에 따라 맛의 차이가 있습니다.",
        },
        {
          title: "일식",
          desc: "신선하고 자연스러운 재료를 사용하여 깔끔하고 아름다운 음식을 만듭니다. 일본 요리는 장식과 조리법에 많은 주의를 기울입니다.",
        },
        {
          title: "양식",
          desc: "서양의 요리 스타일을 의미하며, 주로 유럽과 미국을 기반으로 합니다. 고기, 빵, 치즈, 버터 등이 중요한 재료입니다.",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
// intro__wrap
.intro__inner {
  display: flex;
  justify-content: space-between;
}
.intro__inner {
  display: flex;
  justify-content: space-between;
}
.active {
  display: flex !important;
}
.intro__title {
  width: 33%;
  span {
    background-color: #ff3344;
    font-size: 14px;
    padding: 4px 30px 2px;
    color: #fff;
    border-radius: 40px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
  }
  h3 {
    font-size: 50px;
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 30px;
  }
  p {
    font-size: 18px;
    line-height: 1.5;
    font-weight: 500;
  }
}
.intro__desc {
  width: 66%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  > div {
    width: 48%;
    // background-color: #ccc;
    margin-bottom: 40px;
    > h4 {
      display: inline-block;
      font-size: 24px;
      margin-bottom: 15px;
      font-weight: 700;
    }
    > p {
      font-size: 18 px;
      font-weight: 500;
    }
    &:nth-child(1) {
      margin-bottom: 15px;
    }
  }
}
</style>
