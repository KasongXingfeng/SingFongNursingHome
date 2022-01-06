<template>
  <div class="navbar">
    <div>
      <img class="picture" src="../src/assets/image2.png">
    </div>
    <div class="links">
      <a>組織架構</a>
      <span>|</span>
      <a>服務介紹</a>
      <span>|</span>
      <a>環境介紹</a>
      <span>|</span>
      <a>活動花絮</a>
    </div>
  </div>

  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Orginazation msg2="Welcome to Your Vue.js App"/>
  
  <div class="footer">
    <div class="contact">
      <div class="contact_content">
        <div class="left">
          <div class="contact_title">與我們聯絡</div>
          <div class="contact_subtitle">Contact Us</div>
          <img src="../src/assets/line.png">
        </div>
        <div class="right">
          <div>1232323232</div>
        </div>
      </div>
    </div>
    <div class="privacy"> © 2022 青松健康事業. All Rights Reserved.</div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Orginazation from './components/Orginazation.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Orginazation
  },
  data(){
    return {
      
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #cae9be;
}
.navbar .picture {
  margin: 22px 32px;
}
.navbar .links{
  display: flex;
  column-gap: 24px;
  font-size: 24px;
  line-height: 28px;
  color: #2C2C2C;
  margin-right: 32px;
}
.footer .contact {
  background-color: #CAE9BE;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px 0;
}
.footer .contact .contact_content {
  display: flex;
  align-items: center;
}
.footer .left {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  row-gap: 12px;
  border-right: 4px solid #578369;
  padding-right: 24px;
  margin-right: 24px;
}
.footer .contact .left .contact_subtitle {
  font-weight: bold;
  font-size: 18px;
  line-height: 21px;
  color: #805800;
}
.footer .contact .left .contact_title {
  font-weight: bold;
  font-size: 24px;
  line-height: 28px;
  color: #29471C;
}
.footer .privacy {
  background-color: #578369;
  font-size: 12px;
  line-height: 14px;
  text-align: center;
  color: #ffffff;
  padding: 8px 0;
}
</style>
