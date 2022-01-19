<template>
  <div class="activities">
    <div class="activities_top">
      <div class="topic_title">活動花絮</div>
      <div class="topic_eng">activities</div>
      <div class="title_line"></div>
    </div>
    <div class="activities_content">
      <div class="card">
        <div class="picture"></div>
        <div class="title">23213231</div>
        <div class="line"></div>
      </div>
      <div class="card">
        <div class="picture"></div>
        <div class="title">23213231</div>
        <div class="line"></div>
      </div>
      <div class="card">
        <div class="picture"></div>
        <div class="title">23213231</div>
        <div class="line"></div>
      </div>
    </div>
    <div class="pagination">
      <img style="padding-right: 28px" src="./../assets/img/Back.svg" />
      <span class="page">1</span>
      <span class="selected">2</span>
      <span class="page">3</span>
      <span class="page">4</span>
      <img style="padding-left: 28px" src="./../assets/img/Forward.svg" />
    </div>
  </div>
</template>
<script>
import dataset from '../assets/data.json'
const data = dataset.objectives
export default {
  name: 'Activities',
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
.topic_title {
  font-size: 32px;
  font-weight: bold;
  line-height: 37px;
  color: #29471c;
  margin-bottom: 4px;
}
.topic_eng {
  font-size: 24px;
  font-weight: bold;
  line-height: 28px;
  color: #805800;
  margin-bottom: 10px;
}
.title_line{
  height: 2px;
  width: 58px;
  background-color: #29471c;
}
.activities {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.activities .activities_top {
  width: 60%;
  margin: 72px 50px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.activities_content{
  width: 60%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.activities_content .card{
  background-color: #fff;
  padding: 28px;
  height: 300px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-direction: column;
  row-gap: 24px;
  border: solid 1px #eee;
  box-shadow: 2px 4px 6px rgba(0, 0, 0, 0.25);
}
.activities_content .card .picture{
  width: 265px;
  height: 200px;
  background-color: #ddd;
}
.activities_content .card .title{
  font-size: 24px;
  line-height: 28px;
  color: #2c2c2c;
}
.activities_content .card .line{
  width: 90px;
  height: 1px;
  background-color: #29471C;
}
.pagination{
  background-color: #fff;
  border: 2px solid #CAE9BE;
  box-sizing: border-box;
  border-radius: 99px;
  padding: 18px;
  display: flex;
  align-items: center;
  justify-content: center;
  column-gap: 8px;
  margin: 58px 0;
}

.pagination .page{
  width: 30px;
  height: 30px;
  font-size: 18px;
  line-height: 21px;
  color: #2c2c2c;
  display: flex;
  align-items: center;
  justify-content: center;
}
.selected {
  font-size: 18px;
  color: #ffffff;
  background-color: #578369;
  border-radius: 50%;
  width: 30px;
  height: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
