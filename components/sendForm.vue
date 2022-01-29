<template>
  <b-card class="send-card">
    <div class="card-title"><h4>Send Airtime to Ethiopia</h4></div>
	<div class="card-input px-2">
		<div style="align-self:center;">
			<img src="../assets/flag_et.png" style="width:32px; height: 32px" alt="">
		</div>
		<div style="align-self:center;" class="ml-2">
			<span class=""><b>+251</b></span>
		</div>
		<b-form-input
			id="recieve_amt"
			type="number"
			placeholder="Enter recipent number"
			class="inputs"
		></b-form-input>
	</div>
  <div class="mt-4 mb-1" style="text-align:center;">
    <span><b>Select amount to send</b></span>
  </div>
    <div class="list-header">
      <span>They get</span>
      <span>You pay</span>
    </div>
    <div v-for="item in products" :key="item.price">
      <div
        :class="[item.value == selected ? 'selected' : 'product']"
        v-on:click="selected = item.value"
      >
        <span>ETB {{ item.value }}</span>
        <span>USD {{ item.price }}</span>
      </div>
    </div>
    <div class="form-btn bg-light pb-3 text-center">
      <b-button block size="lg" class="mt-3" variant="success">
        Continue
      </b-button>
    </div>
  </b-card>
</template>

<script>
import flag_et from "../assets/flag_et.png"
export default {
  data() {
    return {
      selected: 1,
      products: [
        { value: 100, price: 2.5, selected: false },
        { value: 200, price: 2.5, selected: false },
        { value: 300, price: 2.5, selected: false },
        { value: 400, price: 2.5, selected: false },
        { value: 500, price: 2.5, selected: false },
        { value: 600, price: 2.5, selected: false },
      ],
    };
  },
};
</script>

<style scoped>
.card-input{
	align-content: center;	
	display: flex;
	flex-direction: row;
	width: auto;
	border: 1.5px solid #cccccc;
}
.inputs{
	border: 0;
	display: inline-block;
	margin-left: 0;
	margin-right: 0;
}
.send-card {
  width: 400px;
  min-width: 300px;
  margin-left: auto;
  margin-right: auto;
  justify-content: center;
}
.card-title {
  text-align: center;
  margin-bottom: 30px;
}
.list-header {
  display: flex;
  justify-content: space-between;
  padding: 0 3%;
  padding-top: 0%;
  margin-bottom: -10px;
  text-align: end;
  color: #999999;
}
.product {
  display: flex;
  justify-content: space-between;
  width: 100%;
  font-weight: 600;
  padding: 2% 3%;
  border: 1.5px solid #cccccc;
  border-radius: 4px;
  background-color: #ffffff;
  margin-top: 15px;
  cursor: pointer;
}
.selected {
  display: flex;
  justify-content: space-between;
  width: 100%;
  font-weight: 600;
  padding: 2% 3%;
  border: 2px solid green;
  border-radius: 4px;
  background-color: #ffffff;
  margin-top: 15px;
  cursor: pointer;
}
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
    -webkit-appearance: none;
    margin: 0;
}
input[type=number]{
    -moz-appearance: textfield;
}
</style>