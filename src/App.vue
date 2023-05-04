<template>
  <div class="app">
    <home-intro />

    <home-moduls />

    <home-events />

  </div>
</template>

<script>
import { defineComponent } from "vue";
import AppLogo from './components/AppLogo/index.vue';
import AppButton from './components/AppButton/index.vue';
import HomeIntro from './components/HomeIntro.vue';
import HomeModuls from './components/HomeModuls.vue';
import HomeEvents from './components/HomeEvents.vue';

export default defineComponent({
  name: 'App',

  components: {
    AppLogo,
    AppButton,
		HomeIntro,
		HomeModuls,
		HomeEvents
  },

  setup() {
    
  },
});
</script>

<style lang="scss">
	* {
		padding: 0;
		margin: 0;
		box-sizing: border-box;
	}

	:root {
		--color-white: #fff;
		--color-grey: #e5e5e5;
		--color-black: #070322;
		--color-blue: #2185fb;
		--color-text: #1E1E2F;
		--color-border: #BDCFE4;
	}

	body {
		font-family: "Roboto", sans-serif;
		background-color: var(--color-grey);
	}

	.container {
		max-width: 1127px;
		margin-left: auto;
		margin-right: auto;
	}
</style>
