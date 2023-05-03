<template>
	<div class="home-moduls">
		<div class="container">
			<div class="home-moduls__inner">
				<h2 class="home-moduls__inner-title">
					В программе предусмотрены <br />
					модули, которые помогут <br />
					прокачать знания по темам:
				</h2>
				<ul class="home-moduls__inner-list">
					<li
						v-for="(item, index) in list"
						:key="index"
						class="home-moduls__inner-item"
					>
						{{ item }}
					</li>
				</ul>
				<div class="home-moduls__btn-group">
					<app-button>Узнать подробнее</app-button>
					<app-button>Смотреть трансляцию</app-button>
					<app-button>Чат участников и организаторове</app-button>
				</div>
			</div>
		</div>
	</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import AppButton from '../components/AppButton/index.vue';

export default defineComponent({
	name: "HomeModuls",

  components: {
    AppButton
  },

	setup() {
		const list = [
      "целевая аудитория компании: как ее выявлять и как с ней работать;",
      "как разработать качественный MVP в минимальные сроки;",
      "основы построения бизнес-модели;",
      "unit-экономика проекта;",
      "работа с инвестициями: секреты общения с инвесторами;",
      "работа с господдержкой и программами;",
      "маркетинг для инноваторов;",
    ];

    return {
      list,
    };
	},
})
</script>

<style lang="scss" scoped>
	.home-moduls {
		background-color: rgb(255, 255, 255);
		background-image: linear-gradient(
			90deg,
			rgba(255, 255, 255, 1) 0%,
			rgba(214, 214, 238, 1) 71%,
			rgba(10, 109, 231, 1) 100%
		);

		&__inner {
			position: relative;
			padding: 314px 0 128px;

			&-title {
				margin-bottom: 30px;
				font-weight: 700;
				font-size: 40px;
				line-height: 140%;
				color: var(--color-black);
			}

			&-list {
				list-style: none;
				margin-bottom: 62px;
			}

			&-item {
				position: relative;
				padding: 10px 0 10px 22px;
				font-size: 24px;
				line-height: 140%;
				color: var(--color-black);
				opacity: 0.89;

				&::before {
					position: absolute;
					content: "";
					width: 10px;
					height: 10px;
					left: 0;
					top: 20px;
					background-color: var(--color-blue);
					border-radius: 50%;
				}
			}
		}

		&__btn-group {
			display: flex;
			gap: 24px;
		}
	}
</style>
