<template>
  <div class="container">
    <div v-if="isMobile" class="tab-title">
      <div class="title">{{ title1 }}</div>
    </div>
    <img :src="image1" class="image-rugby" alt="rugby" />
    <div v-if="!isMobile" class="tab-title">
      <div class="title">{{ title1 }}</div>
    </div>
    <div
      v-for="(item, index) in part1"
      :key="index"
      :class="'tab' + (index + 1)"
    >
      <div class="flex-centent1">
        <div class="label">
          {{ item.number }}
          <p class="attache"></p>
        </div>
        <div class="label-name">{{ item.label }}</div>
      </div>
      <div class="desc">
        {{ item.desc }}
      </div>
    </div>

    <!-- part2 -->
    <div v-if="isMobile" class="tab-title">
      <div class="title">{{ title1 }}</div>
    </div>
    <img :src="image2" class="image-basketball" alt="basketball" />
    <div v-if="!isMobile" class="tab-title">
      <div class="title-part2">{{ title2 }}</div>
    </div>
    <div
      v-for="(item, index) in part2"
      :key="index"
      :class="'tab' + (index + 1) + '-part2'"
    >
      <div class="flex-centent2">
        <div :class="label">
          {{ item.number }}
          <p class="attache"></p>
        </div>
        <div class="label-name">{{ item.label }}</div>
      </div>
      <div class="desc-white">
        {{ item.desc }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "App",

  components: {},
  mounted() {
    this.checkIfMobile();
    window.addEventListener("resize", this.checkIfMobile);
  },
  methods: {
    checkIfMobile() {
      this.isMobile = window.innerWidth <= 767; // กำหนดขนาดเป็น mobile size ตามต้องการ
    },
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.checkIfMobile);
  },
  data: () => ({
    isMobile: false,
    title1: "ATHLETS",
    title2: "PLAYERS",
    image1: require("../src/assets/rugby-desktop.svg"),
    image2: require("../src/assets/basketball-desktop.svg"),
    part1: [
      {
        number: "01",
        label: "CONNECTION",
        desc: "Connect with coaches directly, you can ping coaches to view profile.",
      },
      {
        number: "02",
        label: "COLLABORATION",
        desc: "Work with other student athletes to increase visability. When you share and like other players videos it will increase your visability as a player. This is the team work aspect to Surface 1.",
      },
      {
        number: "03",
        label: "GROWTH",
        desc: "Resources and tools for you to get better as a student Athelte. Access to training classes, tutor sessions, etc ",
      },
    ],
    part2: [
      {
        number: "01",
        label: "CONNECTION",
        desc: "Connect with talented athlete directly, you can watch their skills through video showreels directly from Surface 1.",
      },
      {
        number: "02",
        label: "COLLABORATION",
        desc: "Work with recruiter to increase your chances of findingtalented athlete.",
      },
      {
        number: "03",
        label: "GROWTH",
        desc: "Save your time, recruit proper athlets for your team. ",
      },
    ],
  }),
};
</script>


<style scoped>
body,
html {
  margin: 0;
  padding: 0;
  height: 100%;
}

.container {
  position: relative;
  width: 100%;
  height: 100vh;
}
.flex-centent1 {
  display: flex;
  align-items: center;
}
.flex-centent2 {
  display: flex;
  align-items: center;
}
.tab-title {
  height: 105px;
  color: #ffffff;
  margin-top: 100px;
}
.title {
  color: #e7e7e7;
  font-family: Roboto;
  font-size: 90px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
.title-part2 {
  color: #e7e7e7;
  font-family: Roboto;
  font-size: 90px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

/* tab1 */
.tab1 {
  color: #ffffff;
  height: 210px;
}
.label {
  color: #000;
  font-family: Roboto;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  letter-spacing: 1.5px;
}
.attache {
  width: 22px;
  height: 5px;
  flex-shrink: 0;
  border-radius: 2.5px;
  background: #603ebe;
}
.attache-white {
  width: 22px;
  height: 5px;
  flex-shrink: 0;
  border-radius: 2.5px;
  background: #ffffff;
}
.label-name {
  color: #c2c2c2;
  font-family: Roboto;
  font-size: 36px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  letter-spacing: 1.5px;
  margin-left: 10px;
}
.desc {
  color: #000;
  font-family: Roboto;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 28px;
}
/* close tab1 */

/* tab2 */
.tab2 {
  color: #f5f4f9;
  height: 266px;
}
/* close tab2 */

/* tab3 */
.tab1-part2 {
  color: #ffffff;
  height: 210px;
}
.tab2-part2 {
  color: #f5f4f9;
  height: 210px;
}
.tab3 {
  width: 100%;
  background-color: #5e3db3;
  height: 238px;
}
.tab3-part2 {
  width: 100%;
  background-color: #090c35;
  height: 238px;
}
.label-part2 {
  color: #8f6be8;
  font-family: Roboto;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  letter-spacing: 1.5px;
}
.desc-white {
  color: #fff;
  font-family: Roboto;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 28px;
}
/* close tab3 */

/* Mobile size: 320px to 767px */
@media (min-width: 320px) and (max-width: 767px) {
  /* Adjust styles for mobile-sized screens */
  /* Example styles */
  .container {
    position: relative;
  }
  .image-rugby {
    width: 200px;
    height: 281px;
    display: block;
    margin-right: auto;
    margin-left: auto;
    margin-top: 74px;
  }
  .image-basketball {
    width: 382px;
    height: 249px;
    display: block;
    margin-right: auto;
    margin-left: auto;
    margin-top: 95px;
  }
  .tab-title {
    height: 20px;
    margin-top: 20px;
  }
  .title {
    padding: 0px 20px;
  }
  .tab1 {
    padding: 15px 20px;
  }
  .tab2 {
    padding: 15px 20px;
  }
  .tab3 {
    padding: 60px 20px;
    background: #F5F4F9;
  }
  .tab1-part2 {
     padding: 15px 20px;
  }
  .tab2-part2 {
     padding: 15px 20px;
  }
  .tab3-part2 {
     padding: 60px 20px;
     background: #F5F4F9;
  }
}

/* Tablet size: 768px to 1919px */
@media (min-width: 768px) and (max-width: 1919px) {
  /* Adjust styles for tablet-sized screens */
  /* Example styles */
  .container {
    overflow-x: hidden;
    overflow-y: auto;
  }
  .image-rugby {
    width: 518px;
    height: 699px;
    position: absolute;
    z-index: 2;
    left: -180px;
    top: 90px;
  }
  .image-basketball {
    width: 691px;
    height: 568px;
    position: absolute;
    z-index: 2;
    right: -200px;
  }
  .title {
    padding-left: 290px;
  }
  .tab1 {
    padding-left: 290px;
  }
  .tab2 {
    padding-left: 290px;
  }
  .tab3 {
    padding: 30px 30px 30px 290px;
    height: 178px;
  }
  .title-part2 {
    padding-left: 30px;
  }
  .tab1-part2 {
    margin-top: 45px;
    padding-left: 30px;
    height: 206px;
  }
  .tab2-part2 {
    padding-left: 30px;
    height: 179px;
  }
  .tab3-part2 {
    padding: 30px 30px 30px 30px;
    height: 151px;
  }
  .tab-title {
    margin: 21px 0px 15px 0px;
  }
  .desc {
    width: 447px;
  }
}

/* Desktop size: 1920px and larger */
@media (min-width: 1920px) {
  /* Adjust styles for larger screens (Desktop) */
  /* Example styles */
  .title {
    padding-left: 1008px;
  }
  .tab1 {
    padding-left: 1008px;
  }
  .tab2 {
    padding-left: 1008px;
  }
  .tab3 {
    padding: 60px 0px 60px 1008px;
  }
  .tab1-part2 {
    padding-left: 322px;
  }
  .tab2-part2 {
    padding-left: 322px;
  }
  .tab3-part2 {
    padding: 60px 0px 108px 322px;
    height: 210px;
  }
  .title-part2 {
    padding-left: 322px;
  }
  .tab-title {
    margin: 30px 0px 80px 0px;
  }
  .desc {
    width: 717px;
  }
  .image-rugby {
    padding: 0px 175px;
    max-width: 100%;
    height: auto;
    position: absolute;
    z-index: 2;
  }
  .image-basketball {
    right: 125px;
    max-width: 100%;
    height: auto;
    position: absolute;
    z-index: 2;
  }
}
</style>
