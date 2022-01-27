<template>
  <div class="all">
    <div class="top">
      <div class="left">
      </div>
      <div class="right">
        <div class="right_inside">
          <div class="topic_title">環境介紹</div>
          <div class="topic_eng">Environment</div>
          <div class="title_line"></div>
          <p>本院位處都會，環境清幽，是適合休養的地方。</p>
        </div>
      </div>
    </div>
    <div class="area relax">
      <div class="tag">
        <span class="tag_circle">
          <img src="./../assets/img/bi_house-door-fill.svg" />
        </span>
        <span class="description">休閒區域</span>
      </div>
      <div class="relax_inside">
        <div v-for="item in data" :key="item" class="card">
          <div class="title">{{item.topic}}</div>
          <div class="line"></div>
          <div class="text">{{item.title}}</div>
          <img class="picture" v-bind:src="require('./../assets/environment/' + item.picture + '.jpg')" />
        </div>
      </div>
      <!-- <section>
        <div v-for="(item,index) in data" :key="item">
          <div class="service_top" v-if="index==nowPic">
            <div class="left">
              <img class="picture" v-bind:src="require('./../assets/environment/' + item.picture + '.jpg')" />
            </div>
            <div class="right">
              <div></div>
              <div>
                <div class="relax_topic">{{item.topic}}</div>
                <div class="line"></div>
              </div>
              <p class="title">{{item.title}}</p>
              <div class="dots">
                <span class="dot" v-for="(item,index) in data" :key="item" v-on:click="selectPic(index)" v-bind:class="[nowPic==index?'selected':'unselected']"></span>
              </div>
            </div>
          </div>
        </div>
      </section> -->
    </div>
    <div class="area">
      <div class="room">
        <div class="tag">
          <span class="tag_circle">
            <img src="./../assets/img/Insomnia.svg" />
          </span>
          <span class="description">住房環境</span>
        </div>
        <span style="margin-left: 12px">總床數53床</span>
      </div>
      <div class="pic_set">
        <div class="card">
          <div class="title">獨立單人房</div>
          <div class="line"></div>
          <img src="./../assets/environment/environment_room1.jpg" />
        </div>
        <div class="card">
          <div class="title">多人住房</div>
          <div class="line"></div>
          <img src="./../assets/environment/environment_room2.jpg" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import dataset from '../assets/data.json'
const data = dataset.environments
const nowPic = 0
export default {
  name: 'environment',
  data () {
    return {
      data: data,
      nowPic: nowPic
    }
  },
  methods: {
    selectPic: function (index) {
      this.nowPic = index
    }
  },
  props: {
    msg2: String
  }
}

</script>
<style scoped>
.all .top {
  display: flex;
  width: 100%;
  height: 480px;
}
.all .top .left {
  width: 50%;
  height: 100%;
  background-image: url('../assets/environment/environment_door.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 0 -10px;
  background-color: #eee;
}
.all .right {
  width: 50%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.all .right .right_inside {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 75%;
}
.all .right .right_inside p {
  font-size: 24px;
  line-height: 28px;
  color: #2C2C2C;
  margin-top: 60px;

}
.topic_title {
  font-size: 32px;
  font-weight: bold;
  line-height: 37px;
  color: #2F6098;
  margin-bottom: 4px;
}
.topic_eng {
  font-size: 24px;
  font-weight: bold;
  line-height: 28px;
  color: #888888;
  margin-bottom: 10px;
}
.title_line{
  height: 2px;
  width: 58px;
  background-color: #2F6098;
}
.all {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-bottom: 58px;
}
.area {
  width: 80%;
}
.relax .tag{
  width: 300px;
  border-radius: 99px;
  background-color: #A5D8FF;
  display: flex;
  align-items: center;
  column-gap: 32px;
  padding: 5px 48px 5px 5px;
  margin-top: 72px;
  margin-bottom: 40px;
}
.room .tag{
  width: 300px;
  border-radius: 99px;
  background-color: #A5D8FF;
  display: flex;
  align-items: center;
  column-gap: 32px;
  padding: 5px 48px 5px 5px;
}
.tag_circle{
  background-color: #ffffff;
  width: 45px;
  height: 45px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
}
.description{
  font-size: 18px;
  font-weight: bold;
  line-height: 100%;
  line-height: 21px;
  color: #2C2C2C;
}
.content{
  display: flex;
  align-items: center;
  justify-content: center;
  column-gap: 28px;
  border-top: 1px solid #acacac;
  border-bottom: 1px solid #acacac;
  padding: 36px 28px;
  font-size: 18px;
  line-height: 21px;
  color: #2C2C2C;
  margin-top: 48px;
}
.pic_set {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 100%;
  column-gap: 12px;
}
.pic_set img {
  width: 32%;
}
.indoor_content {
  display: flex;
  flex-direction: column;
  row-gap: 36px;
}
.line {
  height: 4px;
  width: 58px;
  margin: auto;
  background-color: #2F6098;
}
.service_top {
  width: 100%;
  display: flex;
}
.service_top .left {
  height: 400px;
  background-color: #eee;
}
.service_top .left .picture {
  height: 100%;
}
.service_top .right {
  width: 70%;
  height: auto;
  background-color: #A5D8FF;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  padding: 24px 12px;
}
.service_top .right .title {
  font-size: 25px;
  line-height: 28px;
  color: #2C2C2C;
}
.service_top .right .dots {
  display: flex;
  column-gap: 12px;
}
.service_top .right .dot {
  border-radius: 50%;
  width: 12px;
  height: 12px;
  cursor: pointer;
}
.selected {
  background-color: #2F6098;
}
.unselected {
  background-color: #c4c4c4;
}
.relax_topic {
  color: #2F6098;
  font-weight: bold;
  font-size: 28px;
  line-height: 46px;
  margin-bottom: 24px;
}
.room {
  display: flex;
  margin-top: 72px;
  margin-bottom: 40px;
  align-items: center;
}
.pic_set .card {
  background-color: #fff;
  width: 48%;
  padding: 32px 0;
  /* height: 430px; */
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-direction: column;
  /* row-gap: 2px; */
  border: solid 1px #eee;
  box-shadow: 2px 4px 6px rgba(0, 0, 0, 0.25);
}
.card .title {
  font-weight: bold;
  font-size: 24px;
  color: #2F6098;
  margin-bottom: 24px;
}
.pic_set .card img {
  width: 80%;
  margin-top: 24px;
}
.relax .relax_inside{
  display: flex;
  flex-wrap: wrap;
  column-gap: 24px;
  row-gap: 24px;
  justify-content: space-between;
}
.relax .relax_inside .card {
  width: 46%;
  padding: 32px 0;
  border: solid 1px #eee;
  background-color: #fff;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-direction: column;
  box-shadow: 2px 4px 6px rgba(0, 0, 0, 0.25);
}
.relax .relax_inside .card img {
  width: 80%;
  margin-top: 24px;
}
.relax_inside .text {
  font-size: 18px;
  line-height: 21px;
  color: #2C2C2C;
  padding: 20px 10% 0 10%;
  text-align: left;
}
@media screen and (max-width: 768px) {
  .all .top {
    flex-direction: column;
    height: 500px;
  }
  .all .top .left {
    width: 100%;
  }
  .all .top .right {
    width: 100%;
  }
  .all .right .right_inside {
    margin-top: 24px;
  }
  .content {
    margin: 24px 20px 0px 20px;
  }
  .relax .relax_inside .card {
    width: 100%;
  }
  .pic_set .card {
    width: 100%;
  }
  .room {
    flex-direction: column;
    align-items: flex-start;
  }
}
@media only screen and (max-width: 480px) {
  .area {
    width: 90%;
  }
  .topic_title {
    font-size: 30px;
  }
  .topic_eng {
    font-size: 20px;
  }
  .all .right .right_inside p {
    font-size: 16px;
    margin-top: 12px;
  }
  .relax .tag {
    width: 90%;
    margin: 20px auto 12px auto;
  }
  .room .tag {
    width: 90%;
    margin: 20px auto 12px auto;
  }
  .room {
    align-items: center;
  }
  .pic_set{
    flex-direction: column;
  }
  .pic_set img {
    width: 80%;
    padding: 10px;
  }
  .indoor_column {
    align-items: center;
    flex-direction: column;
  }
  .line {
    width: 50%;
    background-color: #2F6098;
  }
  .area .content p {
    font-size: 16px;
  }
  .content {
    margin: 16px 12px 0px 12px;
    padding: 24px 20px;
  }
  .title {
    font-size: 20px;
  }
}
</style>
