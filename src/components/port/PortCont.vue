<template>
  <section id="portSection" class="port__wrap Nanum5">
    <p>세계적으로 유명하고 대표적인 음식 종류</p>
    <div class="port__inner container">
      <div class="port_btn">
        <span class="button portBtn1" @click="changeImageNames('korea')"
          >한식</span
        >
        <span class="button portBtn2" @click="changeImageNames('china')"
          >중식</span
        >
        <span class="button portBtn3" @click="changeImageNames('japan')"
          >일식</span
        >
        <span class="button portBtn4" @click="changeImageNames('american')"
          >양식</span
        >
      </div>
      <div class="port__conts">
        <div class="port mb20">
          <figure class="port__header">
            <img :src="getImagePath('1')" :alt="foodType" />
          </figure>
        </div>
        <div class="port">
          <figure class="port__header">
            <img :src="getImagePath('2')" :alt="foodType" />
          </figure>
        </div>
        <div class="port">
          <figure class="port__header">
            <img :src="getImagePath('3')" :alt="foodType" />
          </figure>
        </div>
        <div class="port">
          <figure class="port__header">
            <img :src="getImagePath('4')" :alt="foodType" />
          </figure>
        </div>
        <div class="port">
          <figure class="port__header">
            <img :src="getImagePath('5')" :alt="foodType" />
          </figure>
        </div>
        <div class="port">
          <figure class="port__header">
            <img :src="getImagePath('6')" :alt="foodType" />
          </figure>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      foodType: "korea",
    };
  },
  methods: {
    changeImageNames(type) {
      this.foodType = type;
    },
    getImagePath(index) {
      return `../../images/port/${this.foodType.toLowerCase()}food_${index}.png`;
    },
  },
};
</script>

<style>
.port__wrap {
  text-align: center;
  padding-bottom: 120px;
}
.port__wrap p {
  padding-bottom: 60px;
}

.port__inner .port_btn {
  margin-bottom: 50px;
}
.port__inner .port_btn span {
  background-color: #eaf0ff;
  padding: 15px 30px;
  margin: 10px;
  border-radius: 30px;
  border: 1px solid #abc3ff;
  transition: background-color 0.3s;
}
.port__inner .port_btn :hover {
  background-color: #b5c8f7;
}
.port__inner .port__conts {
  flex-wrap: wrap;
}
.port__inner .port__conts .port {
  width: 32.3%;
}
.port__inner .port__conts .port .port__header img {
  width: 410px;
  height: 300px;
  object-fit: cover;
  border-radius: 10px;
}
.port__inner .port__conts .port .port__body {
  margin-top: 10px;
  margin-bottom: 50px;
  text-align: left;
  display: flex;
}
.port__inner .port__conts .port .port__body span img {
  margin-top: 5px;
  margin-right: 10px;
  width: 40px;
  height: 40px;
  background-color: #999;
  border-radius: 50%;
}
.port__inner .port__conts .port .port__body .title {
  font-size: 20px;
  color: var(--color_body);
  font-weight: 700;
  line-height: 1.5;
}
.port__inner .port__conts .port .port__body .desc {
  font-size: 16px;
  color: #2c3a4b;
  font-weight: 300;
}
.port__conts {
  display: flex;
  justify-content: space-between;
}

.mb20 {
  margin-bottom: 20px;
}
</style>
