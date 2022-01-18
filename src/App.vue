<template>
  <div class="navbar">
    <div>
    <img class="picture" src="../src/assets/image2.png">
    </div>
    <div class="links">
      <router-link to="/orginazation" class="link">組織架構</router-link>
      <span>|</span>
      <router-link to="/" class="link">服務介紹</router-link>
      <span>|</span>
      <router-link to="/" class="link">環境介紹</router-link>
      <span>|</span>
      <router-link to="/" class="link">活動花絮</router-link>
    </div>
  </div>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/orginazation">orginazation</router-link>
  </div> -->
  <router-view/>
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
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}
#nav a {
  font-weight: bold;
  color: #2c3e50;
}
#nav a.router-link-exact-active {
  color: #42b983;
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
.navbar .links .link{
  color: #2C2C2C;
  text-decoration: none;
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
