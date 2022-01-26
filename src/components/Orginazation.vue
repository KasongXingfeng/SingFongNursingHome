<template>
  <div class="structure">
    <div class="structure_top">
      <div class="topic_title">組織圖</div>
      <div class="topic_eng">Organization Structure</div>
      <div class="title_line"></div>
    </div>
    <div>
      <img class="structure_pic" src="../assets/img/Group15.png">
    </div>
  </div>
</template>

<script>

export default {
  name: 'Orginazation',
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
.structure {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.structure .structure_top {
  width: 80%;
  margin: 102px 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.structure_pic {
  margin-bottom: 84px;
  width: 90%;
}
@media screen and (max-width: 480px) {
  .topic_title {
    font-size: 30px;
  }
  .topic_eng {
    font-size: 20px;
  }
}
</style>
