<template>
	<div class="home-events">
		<div class="container">
			<div class="home-events__inner">
				<h2 class="home-events__inner-title">
					Мероприятия Архипелага в Точках кипения
				</h2>

				<div class="home-events__inner-filters">
					<select class="home-events__inner-filters-select">
						<option selected value="all events">все мероприятия</option>
						<option value="first event">первое мероприятие</option>
						<option value="second event">второе мероприятие</option>
						<option value="third event">третье мероприятие</option>
					</select>

					<select class="home-events__inner-filters-select">
						<option selected value="Moscow">в г. Москва</option>
						<option value="Spb">в г. Спб</option>
						<option value="Kazan">в г. Казань</option>
						<option value="Tver">в г. Тверь</option>
					</select>

					<select class="home-events__inner-filters-select">
						<option selected value="all events">в любое время</option>
					</select>

					<select class="home-events__inner-filters-select">
						<option selected value="all events">на любую тему</option>
					</select>
				</div>

				<div class="home-events__inner-lecture-filters">
					<div class="home-events__inner-lecture-filters-more">Еще фильтры</div>
					<select class="home-events__inner-lecture-filters-date">
						<option selected value="by popularity">По популярности</option>
						<option value="by date">по дате</option>
					</select>
				</div>

				<div class="home-events__inner-lecture"></div>

				<app-button>Показать еще</app-button>
			</div>
		</div>
	</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import AppButton from '../components/AppButton/index.vue';

export default defineComponent({
	name: 'HomeEvents',

	components: {
		AppButton
	},

	setup() {
		
	},
})
</script>

<style lang="scss" scoped>
	.home-events {
		background-color: var(--color-grey);

		&__inner {
			padding: 120px 0;

			&-title {
				margin-bottom: 30px;
				font-weight: 700;
				font-size: 40px;
				line-height: 120%;
				color: var(--color-black);
			}

			&-filters {
				display: flex;
				align-items: center;
				margin-bottom: 30px;

				&-select {
					padding: 7px;
					margin-right: 15px;
					border: 1px solid rgba(80, 73, 73, 0.295);
					border-radius: 4px;
					font-weight: 500;
					font-size: 18px;
					line-height: 24px;
					color: var(--color-blue);
				}
			}

			&-lecture-filters {
				display: flex;
				justify-content: space-between;
				align-items: center;
				margin-bottom: 53px;

				&-more {
					position: relative;
					padding-left: 44px;
					font-weight: 400;
					font-size: 16px;
					line-height: 24px;
					color: var(--color-text);
					&::before {
						content: "";
						position: absolute;
						padding: 11px;
						width: 16px;
						height: 16px;
						top: 0;
						left: 0;
						background-image: url(../assets/images/more-icon.png);
						background-repeat: no-repeat;
					}
				}

				&-date {
					padding: 8px;
					background-color: transparent;
					border: 1px solid var(--color-border);
					border-radius: 3px;
				}
			}
		}
	}
</style>
