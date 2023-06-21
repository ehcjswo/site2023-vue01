<template>
  <section id="sliderSection" :class="attr">
    <div class="slider__inner">
      <swiper
        :slides-per-view="1"
        :space-between="50"
        @swiper="onSwiper"
        @slideChange="onSlideChange"
        :autoplay="{
          delay: 2500,
          disableOnInteraction: false,
        }"
        :modules="modules"
      >
        <swiper-slide v-for="(slider, index) in sliders" :key="index">
          <div class="slider__img">
            <div class="slider s1 container">
              <div class="text">
                <h3 v-html="slider.title"></h3>
                <p v-html="slider.desc"></p>
                <a href="#" class="more button-1">더보기</a>
              </div>
              <div class="img" aria-label="hidden">
                <img :src="slider.iconimage1" :alt="slider.title" />
                <img :src="slider.iconimage2" :alt="slider.title" />
                <img :src="slider.iconimage3" :alt="slider.title" />
              </div>
              <div class="circle" aria-label="hidden">
                <span class="circle c1"></span>
                <span class="circle c2"></span>
                <span class="circle c3"></span>
                <span class="circle c4"></span>
                <span class="circle c5"></span>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
</template>
<script>
import { Autoplay } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
export default {
  props: {
    attr: String,
  },
  data: function () {
    return {
      sliders: [
        {
          title: "Books<br /> broaden <br />minds",
          desc: "책은 우리에게 새로운 가치와 인사이트를 주며,<br /> 인생의 여러 측면을 탐구하는 기회를 제공합니다.",
          iconimage1: "./images/slider/sliderIcon1.png",
          iconimage2: "./images/slider/sliderIcon2.png",
          iconimage3: "./images/slider/sliderIcon3.png",
        },
        {
          title: "Books<br /> broaden <br />minds",
          desc: "책은 우리에게 새로운 가치와 인사이트를 주며,<br /> 인생의 여러 측면을 탐구하는 기회를 제공합니다.",
          iconimage1: "./images/slider/sliderIcon1.png",
          iconimage2: "./images/slider/sliderIcon2.png",
          iconimage3: "./images/slider/sliderIcon3.png",
        },
        {
          title: "Books<br /> broaden <br />minds",
          desc: "책은 우리에게 새로운 가치와 인사이트를 주며,<br /> 인생의 여러 측면을 탐구하는 기회를 제공합니다.",
          iconimage1: "./images/slider/sliderIcon1.png",
          iconimage2: "./images/slider/sliderIcon2.png",
          iconimage3: "./images/slider/sliderIcon3.png",
        },
      ],
    };
  },
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log("slide change");
    };
    return {
      onSwiper,
      onSlideChange,
      modules: [Autoplay],
    };
  },
};
</script>
<style lang="scss">
.swiper {
  overflow: visible;
}
.swiper-pagination {
  bottom: -80px !important;
}
.slider__inner {
  overflow: hidden;
  padding: 100px 0;
  position: relative;
  .slider__img {
    .slider {
      .text {
        h3 {
          font-size: 110px;
          font-weight: 800;
          text-transform: uppercase;
          line-height: 1;
          margin-bottom: 40px;
        }
        p {
          font-size: 24px;
          line-height: 1.3;
          margin-bottom: 50px;
        }
        .more {
          font-size: 18px;
        }
      }
      .img {
        position: absolute;
        right: 0;
        top: -120px;
        width: 600px;
        height: 600px;
        background-image: url(@/assets/images/slider/sliderIBg.png);
        background-size: cover;
        img {
          &:nth-child(1) {
            position: absolute;
            width: 300px;
          }
          &:nth-child(2) {
            position: absolute;
            width: 300px;
            right: 0;
            bottom: 140px;
          }
          &:nth-child(3) {
            position: absolute;
            width: 300px;
            bottom: 0;
            left: 30px;
          }
        }
      }
      .circle {
        span {
          display: block;
          position: absolute;
          left: 50%;
          top: 50%;
          width: 20px;
          height: 20px;
          border-radius: 50%;
        }
        span:nth-child(1) {
          background-color: var(--button_blue);
          left: 50%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(2) {
          background-color: var(--button_red);
          top: 20%;
          left: -10%;
          width: 40px;
          height: 40px;
        }
        span:nth-child(3) {
          background-color: var(--button_green);
          left: 100%;
          top: 10%;
        }
        span:nth-child(4) {
          background-color: var(--button_red);
          left: 17%;
          top: -10%;
          width: 10px;
          height: 10px;
        }
        span:nth-child(5) {
          background-color: var(--button_blue);
          left: 90%;
          top: 80%;
          width: 30px;
          height: 30px;
        }
      }
    }
  }
  .slider__btn {
    > a {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      width: 22px;
      height: 40px;
      transition: opacity 0.3s;
      &:hover {
        opacity: 0.5;
      }
    }
    .left {
      left: 20px;
      background-image: url(@/assets/images/slider/slider_left.png);
    }
    .right {
      right: 20px;
      background-image: url(@/assets/images/slider/slider_right.png);
    }
  }
  .slider__dot {
    position: absolute;
    left: 50%;
    bottom: -80px;
    transform: translateX(-50%);
    a {
      display: inline-block;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      margin: 0 5px;
      border: 4px solid #ff3344;
      background-color: #ff3344;
      box-shadow: 0 0 0 3px transparent;
      &.active {
        box-shadow: 0 0 0 3px #ff3344;
        border-width: 4px;
        background-color: #fff;
      }
    }
  }
}
</style>
