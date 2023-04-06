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

					<p class="intro__inner-span">
						Основные мероприятия Архипелага будут проходить в Великом Новгороде, но вы сможете подключиться к трансляции событий в Точках кипения по всей стране.
					</p>

				</div>
			</div>
		</div>

		<div class="moduls">
			<div class="container">
				<div class="moduls__inner">
					<h2 class="moduls__inner-title">
						В программе предусмотрены <br> модули, которые помогут <br> прокачать знания по темам:
					</h2>
					<ul class="moduls__inner-list">
						<li
							v-for="(item, index) in list"
							:key="index"
							class="moduls__inner-item"
						>
							{{ item }}
						</li>
					</ul>
          <div class="moduls__btn-group">
            <app-button>Узнать подробнее</app-button>
            <app-button>Смотреть трансляцию</app-button>
            <app-button>Чат участников и организаторове</app-button>
          </div>

				</div>
			</div>
		</div>

    <div class="events">
      <div class="container">
        <div class="events__inner">
          <h2 class="events__inner-title">
            Мероприятия Архипелага в Точках кипения
          </h2>

          <div class="events__inner-filters">
            <select class="events__inner-filters-select"> 
              <option selected value="all events">все мероприятия</option> 
              <option value="first event">первое мероприятие</option> 
              <option value="second event">второе мероприятие</option> 
              <option value="third event">третье мероприятие</option> 
            </select>

            <select class="events__inner-filters-select"> 
              <option selected value="Moscow">в г. Москва</option> 
              <option value="Spb">в г. Спб</option> 
              <option value="Kazan">в г. Казань</option> 
              <option value="Tver">в г. Тверь</option> 
            </select>

            <select class="events__inner-filters-select"> 
              <option selected value="all events">в любое время</option> 
            </select>

            <select class="events__inner-filters-select"> 
              <option selected value="all events">на любую тему</option>  
            </select>
          </div>

          <div class="events__inner-lecture-filters">
            <div class="events__inner-more-filters"></div>
            <select class="events__inner-date-filters">
              <option selected value="by popularity">по популярности</option> 
              <option value="by date">по дате</option>
            </select>
          </div>

          <div class="events__inner-lecture">

          </div>

          <app-button>Показать еще</app-button>
        </div>
      </div>
    </div>

	</div>
</template>

<script>
	import { defineComponent } from 'vue'
	import AppLogo from './components/AppLogo/index.vue'
  import AppButton from './components/AppButton/index.vue'

	export default defineComponent({
		name: 'App',
		components: {
			AppLogo,
      AppButton
		},
		setup() {
			const list = [
				'целевая аудитория компании: как ее выявлять и как с ней работать;',
				'как разработать качественный MVP в минимальные сроки;',
				'основы построения бизнес-модели;',
				'unit-экономика проекта;',
				'работа с инвестициями: секреты общения с инвесторами;',
				'работа с господдержкой и программами;',
				'маркетинг для инноваторов;'
			]

			return {
				list
			}
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

		&::after {
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

.moduls {
  background-color: rgb(255,255,255);
  background-image: linear-gradient(90deg, rgba(255,255,255,1) 0%, rgba(214,214,238,1) 71%, rgba(10,109,231,1) 100%);

	&__inner {
		position: relative;
		padding: 314px 0 128px;
    
		&-title {
			margin-bottom: 30px;
			font-weight: 700;
			font-size: 40px;
			line-height: 140%;
			color: #070322;
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
			color: #070322;
			opacity: 0.89;

			&::before {
				position: absolute;
				content: "";
				width: 10px;
				height: 10px;
				left: 0;
				top: 20px;
				background-color: #2185FB;
				border-radius: 50%;
			}
		}
	}

  &__btn-group {
      display: flex;
      gap: 24px;
    }
}

.events {
  background-color: #e5e5e5;

  &__inner {
    padding: 120px 0;

    &-title {
      margin-bottom: 30px;
      font-weight: 700;
      font-size: 40px;
      line-height: 120%;
      color: #070322;
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
        color: #2185FB;
      }
    }
  }
}

</style>

