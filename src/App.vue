<template>
  <div class="container">
    <img
      class="image-rugby"
      src="../src/assets/rugby-desktop.svg"
      alt="rugby "
    />
    <div class="tab-title">
      <div class="title">ATHLETS</div>
    </div>
    <div class="tab1">
      <div class="flex-centent1">
        <div class="label">
          01
          <p class="attache"></p>
        </div>
        <div class="label-name">CONNECTION</div>
      </div>
      <div class="desc">
        Connect with coaches directly, you can ping coaches to view profile.
      </div>
    </div>
    <div class="tab2">
      <div class="flex-centent1">
        <div class="label">
          02
          <p class="attache"></p>
        </div>
        <div class="label-name">COLLABORATION</div>
      </div>
      <div class="desc">
        Work with other student athletes to increase visability. When you share
        and like other players videos it will increase your visability as a
        player. This is the team work aspect to Surface 1.
      </div>
    </div>
    <div class="tab3">
      <div class="flex-centent1">
        <div class="label">
          03
          <p class="attache-white"></p>
        </div>
        <div class="label-name">GROWTH</div>
      </div>
      <div class="desc-white">
        Resources and tools for you to get better as a student Athelte. Access
        to training classes, tutor sessions, etc
      </div>
    </div>
    <!-- part2  -->
    <img
      class="image-basketball"
      src="../src/assets/basketball-desktop.svg"
      alt="basketball "
    />
    <div class="tab-title">
      <div class="title-part2">PLAYERS</div>
    </div>
    <div class="tab1-part2">
      <div class="flex-centent2">
        <div class="label">
          01
          <p class="attache"></p>
        </div>
        <div class="label-name">CONNECTION</div>
      </div>
      <div class="desc">
        Connect with talented athlete directly, you can watch their skills
        through video showreels directly from Surface 1.
      </div>
    </div>
    <div class="tab2-part2">
      <div class="flex-centent2">
        <div class="label">
          02
          <p class="attache"></p>
        </div>
        <div class="label-name">COLLABORATION</div>
      </div>
      <div class="desc">
        Work with recruiter to increase your chances of finding talented
        athlete.
      </div>
    </div>
    <div class="tab3-part2">
      <div class="flex-centent2">
        <div class="label-bottom">
          03
          <p class="attache-white"></p>
        </div>
        <div class="label-name">GROWTH</div>
      </div>
      <div class="desc-white">
        Save your time, recruit proper athlets for your team.
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    //
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

.image-rugby {
  position: absolute;
  z-index: 2;
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
.label-bottom {
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
.image-basketball {
  position: absolute;
  z-index: 2;
}
/* close tab3 */

/* Media Queries เพื่อปรับแต่งสไตล์ตามขนาดหน้าจอที่ต่างกัน */
@media only screen and (min-width: 1920px) {
  /* ปรับแต่งสไตล์สำหรับขนาดหน้าจอ 1920px */
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
  }
  .image-basketball {
    right: 125px;
    max-width: 100%;
    height: auto;
  }
}

@media only screen and (max-width: 1919px) and (min-width: 769px) {
  /* ปรับแต่งสไตล์สำหรับขนาดหน้าจอ 768px - 1920px */
  .container {
    overflow-x: hidden;
    overflow-y: auto; 
  }
  .image-rugby {
    width: 518px;
    height: 699px;
    position: absolute;
    z-index: 1;
    left: -180px;
    top: 90px;
  }
  .image-basketball {
    width: 691px;
    height: 568px;
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

@media only screen and (max-width: 768px) and (min-width: 321px) {
  /* ปรับแต่งสไตล์สำหรับขนาดหน้าจอ 320px - 768px */
  /* ... */
}

@media only screen and (max-width: 320px) {
  /* ปรับแต่งสไตล์สำหรับขนาดหน้าจอน้อยกว่าหรือเท่ากับ 320px */
  /* ... */
}
</style>
