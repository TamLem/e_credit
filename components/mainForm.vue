<template>
  <div class="form-container">
    <div class="form-header">
      <span>Exchange Rate</span>
      <h3>1 EUR = 122.98464 KES</h3>
    </div>
    <div class="form-inputs bg-light py-3 px-2">
      <b-input-group prepend="You send" class="mt-3">
		  <b-input-group-prepend></b-input-group-prepend>
        <b-form-input
          id="send_amt"
          type="number"
          placeholder="100.00"
          class="inputs"
        ></b-form-input>
        <b-input-group-append>
          <b-form-select v-model="selected" :options="currencies" class="inputs cur_select">
          </b-form-select>
        </b-input-group-append>
      </b-input-group>
	   <b-input-group prepend="They get" class="mt-3">
        <b-form-input
          id="recieve_amt"
          type="number"
          placeholder="100.00"
          class="inputs"
        ></b-form-input>
        <b-input-group-append>
          <b-form-select v-model="selected" :options="currencies" class="inputs cur_select">
          </b-form-select>
        </b-input-group-append>
      </b-input-group>
    </div>
	<div class="form-btn bg-light pb-3 text-center">
		<b-button size="lg" class="mt-3" variant="success">
			Continue
		</b-button>
	</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: "USD",
      currencies: [
        { value: "USD", text: "USD" },
        { value: "EUR", text: "EUR" },
      ],
    };
  },
};
</script>

<style scoped>
.form-header{
	text-align: center;
	color: white;
	background: linear-gradient(90deg, rgb(40,167,68) 13%, rgb(31,126,53));
}
.form-container {
  color: aquamarine;
  width: 350px;
  height: auto;
  display: flex;
  flex-direction: column;
  justify-content: right;
  right: 15%;
  border-radius: 10px;
  overflow: hidden;
}
.inputs{
	display: inline-block;
	border: 3px solid rgb(31,126,53);
	border-right: none;
	border-left: none;
	height: 3em;
}
.cur_select{
	background: rgb(31,126,53);
	color: white;
}

.input-group-text{
	background: none;
	color: black;
	border: 3px solid rgb(31,126,53);
  	border-radius: 10px;
	border-right: none;

}
</style>