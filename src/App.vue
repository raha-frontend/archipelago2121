<template>
	<div class="app">
		<div class="intro">
			<div class="container">
				<div class="intro__inner">

					<div class="intro__inner-logo">
						<app-logo />
					</div>

					<h1 class="intro__inner-title">Архипелаг 2121</h1>

					<p class="intro__inner-desc">
						Приглашаем принять участие в Архипелаге 2121 — проектно-образовательном интенсиве для индивидуальных участников, стартапов, регионов и вузов, которые развивают проекты в сфере новых технологий. На событии соберутся лучшие цифровые команды со всей страны.
					</p>

					<span class="intro__inner-span">
						Основные мероприятия Архипелага будут проходить в Великом Новгороде, но вы сможете подключиться к трансляции событий в Точках кипения по всей стране.
					</span>

				</div>
			</div>
		</div>
	</div>
</template>

<script>
	import { defineComponent } from 'vue'
	import AppLogo from './components/AppLogo/index.vue'

	export default defineComponent({
		name: 'App',
		components: {
			AppLogo
		}
	})
</script>

<style lang="scss">

* {
	padding: 0;
	margin: 0;
	box-sizing: border-box;
}

 body {
	 font-family: 'Roboto', sans-serif;
	 min-width: 1440px;
	 margin-right: auto;
	 margin-left: auto;
	 background-color: #eee;
 }

 .container {
	 max-width: 1127px;
	 margin-left: auto;
	 margin-right: auto;
 }

.intro {
	background-image: linear-gradient(105.25deg, #001377 0%, #1633CF 100%);
	&__inner {
		position: relative;
		padding: 48px 0 344px;
		::after {
			position: absolute;
			content: "";
			width: 760px;
			height: 754px;
			left: 536px;
			top: 32px;
			background-image: url(./assets/images/unicorn.png);
			background-repeat: no-repeat;
		}

		&-logo {
			height: 56px;
			margin-bottom: 90px;
		}

		&-title {
			margin-bottom: 24px;
			font-weight: 700;
			font-size: 72px;
			line-height: 92px;
			color: #FFFFFF;
		}

		&-desc {
			margin-bottom: 16px;
			max-width: 648px;
			font-weight: 400;
			font-size: 24px;
			line-height: 140%;
			color: #FFFFFF;
		}

		&-span {
			display: block;
			max-width: 648px;
			font-weight: 400;
			font-size: 24px;
			line-height: 140%;
			color: #FFFFFF;
		}
	}
}

</style>

