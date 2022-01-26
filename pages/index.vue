<template>
<div class="container">
	<navbar />
	<b-jumbotron header="BootstrapVue" text-variant="white" lead="Bootstrap v4 Components for Vue.js 2">
		<p>For more information visit website</p>
		<b-button variant="primary" href="#">More Info</b-button>
		<main-form />
 	</b-jumbotron>
	<section class="info-banner">

	</section>
	<section class="info-banner">

	</section>
</div>

</template>

<script>
import MainForm from '../components/mainForm.vue'
import navbar from '../components/navbar.vue'
export default {
  components: { navbar, MainForm },

}
</script>

<style>
	body {
		background-color: #f8f7f2;
	}
	.jumbotron {
		background-image: url("../assets/hero_bg.png");
		height: 50vh;
	}
	.info-banner {
		height: 25vh;
		margin-bottom: 20px;
		background: linear-gradient(90deg, rgb(129, 63, 214), rgb(61, 17, 82));
	}
</style>