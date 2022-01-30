<template>
  <div class="container_order container-fluid">
    <div class="order_form">
      <div style="border-bottom: 1px solid #ccc" class="pb-3">
        <h2>Select payment method</h2>
      </div>
      <div class="select_method mt-3 pb-4 mb-1" style="">
        <div id="card_select" v-on:click="paymentMethod = 'card'">
          <h4>Card payment</h4>
        </div>
        <div id="paypal_select" v-on:click="paymentMethod = 'paypal'">
          <h4>PayPal</h4>
        </div>
      </div>
      <br />
      <div v-show="paymentMethod == 'card'" id="payment-card">
          <keep-alive>
            <paypal />
          </keep-alive>
      </div>
      <div v-show="paymentMethod == 'paypal'" id="payment-paypal">
        <img
          src="https://www.paypalobjects.com/webstatic/mktg/logo/AM_SbyPP_mc_vs_dc_ae.jpg"
          border="0"
          alt="PayPal Acceptance Mark"
        />
      </div>
    </div>
    <div class="order_summary">
      <div style="border-bottom: 1px solid #ccc" class="pb-3">
        <h2>Your Order</h2>
      </div>
      <br style="color: white" />
      <div style="border-bottom: 1px solid #ccc">
        <div class="push_apart">
          <p>ETB 450 to +2519125486</p>
          <span>8.50 $</span>
        </div>
        <div class="push_apart">
          <p>Our fee</p>
          <span>0 $</span>
        </div>
      </div>
      <div
        class="push_apart mt-4 pb-4 mb-3"
        style="border-bottom: 1px solid #ccc"
      >
        <b><span>Total</span></b
        ><b><span>8.50 $</span></b>
      </div>
      <div class="mt-5">
        <p style="color: #555; font-size: 0.9rem; text-align: justify">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque
          laudantium soluta culpa unde repellat quae? lorem20
        </p>
        <p style="color: #555; font-size: 0.9rem; text-align: justify">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque
          laudantium soluta culpa unde repellat quae? lorem20
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import  paypal from "../components/paypal.vue";

export default {
  components: {paypal},
  data() {
    return {
      paymentMethod: "card",
    };
  },
};
</script>
	
<style lang="css" scoped>
label {
  text-align: left;
}

.container_order {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap-reverse;
  justify-content: space-between;
  width: 80%;
  margin-top: 10%;
  /* margin: 20% 10% 20% 10%; */
}
.order_form {
  background-color: white;
  padding: 2.5%;
  width: 60%;
  text-align: center;
  margin-right: 1%;
  height: auto;
}
.select_method {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  padding-left: 15%;
  padding-right: 15%;
  border-bottom: 1px solid #ccc;
}
#card_select {
  cursor: pointer;
  background: black;
  color: white;
  padding: 1.5rem;
}
#paypal_select {
  cursor: pointer;
  background: black;
  color: white;
  padding: 1.5rem;
}
.order_summary {
  background: white;
  width: 35%;
  text-align: center;
  padding: 2.5%;
  margin-left: 1%;
  margin-bottom: auto;
}
.push_apart {
  display: flex;
  justify-content: space-between;
  margin: 5px 5px;
}
</style>>

</style>