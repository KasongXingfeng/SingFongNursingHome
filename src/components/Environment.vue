<template>
  <div class="all">
    <div class="area">
      <div class="tag">
        <span class="tag_circle">
          <img src="./../assets/img/CloseUp.svg" />
        </span>
        <span class="description">戶外休閒區</span>
      </div>
      <div class="content">
        <p>房舍外有步道，周圍有種植花草，供住民平時活動、日光浴，慢活樂趣。</p>
      </div>
    </div>
    <div class="area">
      <div class="tag">
        <span class="tag_circle">
          <img src="./../assets/img/bi_house-door-fill.svg" />
        </span>
        <span class="description">院內環境</span>
      </div>
    </div>
    <div class="area">
      <div class="tag">
        <span class="tag_circle">
          <img src="./../assets/img/Insomnia.svg" />
        </span>
        <span class="description">寢室環境</span>
      </div>
      <div class="content">
        <p>寢室格局有雙人房、六人房，皆有獨立廁所、冷氣，配備床、床旁桌、頭燈、圍簾，以及個人獨立衣櫥，收納空間相當充足。</p>
      </div>
    </div>
  </div>
</template>
<script>
import dataset from '../assets/data.json'
const data = dataset.objectives
export default {
  name: 'environment',
  data () {
    return {
      data: data
    }
  },
  props: {
    msg2: String
  }
}

</script>
<style scoped>
.all {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-bottom: 58px;
}
.area {
  width: 60%;
}
.tag{
  width: 200px;
  border-radius: 99px;
  background-color: #CAE9BE;
  display: flex;
  align-items: center;
  column-gap: 32px;
  padding: 5px 48px 5px 5px;
  margin-top: 72px;
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
</style>
