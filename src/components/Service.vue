<template>
  <div class="client">
    <div class="client_top">
      <div class="topic_title">服務對象</div>
      <div class="topic_eng">Client</div>
      <div class="title_line"></div>
    </div>
    <div class="client_content">
      <div class="columns" id="app">
        <div class="column" v-for="item in client" :key="item">
          <span class="client_circle">
            <img style="width:32px" src="./../assets/img/carbon_airline-passenger-care.svg">
          </span>
          <span class="description">{{ item.content }}</span>
        </div>
      </div>
    </div>
  </div>
    <div class="charges">
    <div class="charges_top">
      <div class="topic_title">收費標準</div>
      <div class="topic_eng">charges</div>
      <div class="title_line"></div>
    </div>
    <div class="charges_content">
      <div class="box" v-for="item in charges" :key="item">
        <div class="tag">
          <span class="client_circle">
            <img v-bind:src="item.icon">
          </span>
          <span class="description">{{ item.charge }}</span>
        </div>
        <div class="box_inside">
          <div class="detail" v-for="detail in item.charge_item" :key="detail">
            <span>{{detail.item_name}}</span>
            <span>{{detail.price}}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import dataset from '../assets/data.json'
const client = dataset.client
const charges = dataset.charges
export default {
  name: 'service',
  data () {
    return {
      client: client,
      charges: charges
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
.client {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.client .client_top {
  width: 77%;
  margin: 102px 42px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.client_content {
  width: 77%;
}
.client_content .columns {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  row-gap: 24px;
}
.client_content .column {
  width: 47%;
  border-radius: 99px;
  background-color: #CAE9BE;
  display: flex;
  align-items: center;
  column-gap: 12px;
  padding: 5px;
}
.client_content .client_circle{
  background-color: #ffffff;
  width: 45px;
  height: 45px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
}
.client_content .description{
  font-size: 18px;
  line-height: 21px;
  /* padding: 5px 0; */
  color: #2C2C2C;
}
.charges {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.charges .charges_top {
  width: 77%;
  margin: 102px 42px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.charges_content {
  width: 77%;
}
.charges_content .box{
 border: solid 1px #ACACAC;
 border-radius: 8px;
}
</style>
