<template>
  <div class="container-fluid p-0">
    <div class="section section1">
      <div class="jb-left px-20">
        <h3>Send Mobile Credit to Ethiopia</h3>
        <p></p>
        <div class="partners">
          <h4>Secure Payment</h4>
          <img
            src="https://www.paypalobjects.com/webstatic/mktg/logo/AM_SbyPP_mc_vs_dc_ae.jpg"
            border="0"
            alt="PayPal Acceptance Mark"
          />
        </div>
      </div>
      <div class="right">
        <send-form />
      </div>
    </div>
    <section class="section2"></section>
    <section class="section3"></section>
  </div>
</template>

<script>
import MainForm from "../components/mainForm.vue";
import navbar from "../components/navbar.vue";
import SendForm from "../components/sendForm.vue";
export default {
  components: { navbar, MainForm, SendForm },
};
</script>

<style>
body {
  background-color: #f8f7f2;
}
.section1 {
  background-image: url("../assets/hero_bg.png");
  min-height: 65vh;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap-reverse;
  justify-content: space-evenly;
  align-items: initial;
  padding: 5vw;
}
.jb-left {
  color: white;
}
.section2 {
  height: 50vh;
  width: 100vw;
  justify-content: center;
  padding: 20px;
  background: linear-gradient(90deg, rgb(40, 167, 68) 13%, rgb(31, 126, 53));
}
.section3 {
  height: 35vh;
  margin-bottom: 20px;
}
.inputs {
  display: inline;
  height: 3em;
}
input[type="text"]:focus {
  border: none;
  box-shadow: none;
}
</style>